# Hello, World! #

In this tutorial we will use everything that was learned from the following articles:
  * [Anatomy of a Mission](EMS_Tut_Anatomy.md)
  * [Script Structure](EMS_Tut_Structure.md)
  * [Script Event List](EMS_Tut_Events.md)
  * [Mission Properties](EMS_Tut_Properties.md)
  * [Signal Handling](EMS_Tut_Signals.md)
  * [Primary Objects](EMS_Tut_Primary_Object.md)
  * [Auto-Updates, Looping and Waits](EMS_Tut_Updates.md)
to create a very basic mission.

The mission in a nutshell: Locate one of 3 randomly placed Navigation Beacons in Home of Light and destroy it.

This tutorial was created with X-Studio. X-Studio is recommended for all mission development.

## Setting up the Mission Script ##
First things first, we need to create the Mission Script. With EMS a template mission script has been provided, Simply open up the _"icdm.module.template.missionscript"_ script and save it as whatever you wish to name the mission script, i reccomend leaving most of the name intact and simply changing the module name like so: "_icdm.module.**tutorial**.missionscript.xml_"

## The Setup Event ##
Now that we have made a clone of the template mission script, its time to begin writing our mission. Because this mission is mostly just creation of objects and handling of signals, the bulk of the missions functional code is right here in the setup event.

> #### Creating the Navigational Beacons ####
> First in our setup event, lets create our Navigation Beacons and store them as a mission property so that we can deal with them later on.
```
$missionSector = $Mission[1]
$navBeaconCount = 3
$navBeacons = array alloc: size=0
while $navBeaconCount > 0
   dec $navBeaconCount
   $cNavBeacon.X = random value between -50000 and 50000
   $cNavBeacon.Y = random value between -50000 and 50000
   $cNavBeacon.Z = random value between -50000 and 50000
   $cNavBeacon = create ship: type={Neutral Race Navigational Beacon} owner=[Neutral Race] addto=$missionSector x=$cNavBeacon.X y=$cNavBeacon.Y z=$cNavBeacon.Z
   $cNavBeacon-> set relation against [PLAYERSHIP] to [Foe]
   $cNavBeacon-> set name to 'Hello, World!'
   = [THIS]->call script 'icdm.mission.regsignal': targetMission=$Mission targetObject=$cNavBeacon eventName='SIGNAL_NAVBEACON_KILLED' signal=[SIGNAL_KILLED]
   append $cNavBeacon to array $navBeacons
end
= [THIS]->call script 'icdm.mission.set.property': targetMission=$Mission propertyName='navBeacons' value=$navBeacons
```
> The first thing your probably going to notice is the first line. What were doing here is retrieving the Primay Object of the mission, in this case - when the mission is started the primary object is set to the sector "Home of Light" - you will get to see this in the next tutorial. (see [Array Documentation](EMS_ArrayDocs.md) for mission array indexes)

> The seccond thing your likely to notice is the call to _"icdm.mission.regsignal"_. As per the mission objective, we need to know when the Navigational Beacon's are killed! This call sets up the signal dispatching in such a way that our mission will recieve the event _"SIGNAL\_NAVBEACON\_KILLED"_ when one of the beacons is killed. (See the [Signal Handling](EMS_Tut_Signals.md) article for more information on signals)

> #### Starting Auto-Updates ####
> To demonstrate the use of Auto Updates were going to tell the mission system that this mission wants to receive updates with the following script call:
```
= [THIS]-> call script 'icdm.mission.set.autoupdate' : targetMission=$Mission autoUpdate=[TRUE] updateInterval=10
```

> #### The Final Setup Code ####
> For now, this is all thats needed in our Setup event - we will go over some more advanced things such as mission icons and the DLL overlay in the advanced section of the tutorial.
```

* *******************************************
* ***************EVENT_SETUP*****************
* *******************************************
event_Setup:
   $missionSector = $Mission[1]
   $navBeaconCount = 3
   $navBeacons = array alloc: size=0
   while $navBeaconCount > 0
      dec $navBeaconCount
      $cNavBeacon.X = random value between -50000 and 50000
      $cNavBeacon.Y = random value between -50000 and 50000
      $cNavBeacon.Z = random value between -50000 and 50000
      $cNavBeacon = create ship: type={Neutral Race Navigational Beacon} owner=[Neutral Race] addto=$missionSector x=$cNavBeacon.X y=$cNavBeacon.Y z=$cNavBeacon.Z
      $cNavBeacon-> set relation against [PLAYERSHIP] to [Foe]
      $cNavBeacon-> set name to 'Hello, World!'
      = [THIS]->call script 'icdm.mission.regsignal': targetMission=$Mission targetObject=$cNavBeacon eventName='ON_NAVBEACON_KILLED' signal=[SIGNAL_KILLED]
      append $cNavBeacon to array $navBeacons
   end
   = [THIS]->call script 'icdm.mission.set.property': targetMission=$Mission propertyName='navBeacons' value=$navBeacons

   = [THIS]-> call script 'icdm.mission.set.autoupdate' : targetMission=$Mission autoUpdate=[TRUE] updateInterval=10
endsub
```

## Implementing SIGNAL\_NAVBEACON\_KILLED ##
> #### Creating the Subroutine ####
> Above, we just told the mission system we want to recieve a new event, called _"SIGNAL\_NAVBEACON\_KILLED"_ when a Navigational Beacon dies. Now we need to implement it!

> First we need to make a new subroutine, so at the end of the file were going to insert the following:
```
* *******************************************
* *********SIGNAL_NAVBEACON_KILLED***********
* *******************************************
signal_NavBeaconKilled:
endsub
```

> Now that we have our subroutine, we need to call it - so at the top of the mission script, we are going to add the event to the else-if stack that dispatches signals:
```
if $eventName == 'EVENT_SETUP'
  gosub event_Setup:
else if $eventName == 'EVENT_UPDATE'
  gosub event_Update:
else if $eventName == 'EVENT_ON_PLAYER_ENTER_AREA'
  gosub event_onPlayerEnterArea:
else if $eventName == 'EVENT_MISSION_ENDED'
  gosub event_onMissionEnded:
else if $eventName == 'SIGNAL_NAVBEACON_KILLED'
  gosub signal_NavBeaconKilled:
end
```

> There we go, Now our signal will be dispatched to the correct subroutine. You may notice that my else-if stack has less entries then yours (if you have been following along). This is because ive removed all the events that are not relevant to this mission for the sake of both readability and performance.

> #### Implementing the Signal ####
> This signal is actually very basic, all we need to do is check the killer, and if the killer is the player ship, end the mission as successful, otherwise end as neutral. Oh, and we also throw a small reward for the player in too!
```
* *******************************************
* *********SIGNAL_NAVBEACON_KILLED***********
* *******************************************
signal_NavBeaconKilled:
   *fetch the killer from the event args
   $killer = $eventArgs[1]
   if $killer == [PLAYERSHIP]
      = [THIS]->call script 'icdm.mission.set.reward': targetMission=$Mission rewardValue=100000 addMode=[TRUE]
      = [THIS]->call script 'icdm.mission.end': targetMission=$Mission Success=[TRUE] Failure=null
   else
      = [THIS]->call script 'icdm.mission.end': targetMission=$Mission Success=null Failure=null
   end
endsub
```
> And there we go! if a Navigation Beacon dies to the player ship, the mission will now end in a Success, if a Navigation Beacon dies for any other reason, the mission simply ends, This mission cant "fail" in the traditional sense. _An exercise for the reader: Make the mission Fail if the player is within the same sector as the mission and is not the killer of the beacon._

## The Update Event ##
If you recall, back in the setup event we registered our mission to receive automatic updates from the mission system. What were going to do here is create a sort of "Your getting Hotter", "Your getting Colder" output in the subtitle text of the game. This is one of thoes rare events were we actually require a very high update resolution so were going to use a loop to achieve this.

The update event is not actually necessary for this mission to work, this was added to demonstrate how to use the auto-update system, the mission can quite happily work without this code.

> #### Setting up the basic update loop ####
> > What were doing here is simply copying the basic update loop from the [Auto-Updates, Looping and Waits](EMS_Tut_Updates.md) article and modifying it slightly, it will now exit if the player is not in the mission sector.
```
$missionSector = $Mission[1]
while [TRUE]
   $missionState = $Mission[7]
   $newVersion = is a new script version available
   $playerSector = [PLAYERSHIP]->get sector
   do if $missionState != 1 or $newVersion or $playerSector != $missionSector
      break

   = wait 500 ms
end
```



> #### Adding the functionality ####
> > For this part of the tutorial, ive added comments to the code rather then trying to explain it part by part.
```
* *******************************************
* ***************EVENT_UPDATE****************
* *******************************************
event_Update:
   *#Fetch the missions sector
   $missionSector = $Mission[1]

   *#Fetch the Navigation Beacon array we defined earlier
   $navBeacons = [THIS]->call script 'icdm.mission.get.property': targetMission=$Mission propertyName='navBeacons'

   *#Set the players last distance to 0
   $lastDistance = 0
   while [TRUE]
      $missionState = $Mission[7]
      $newVersion = is a new script version available
      $playerSector = [PLAYERSHIP]->get sector
      do if $missionState != 1 or $newVersion or $playerSector != $missionSector
         break

      *#Set the closest distance to something insanely large at fisrt!
      $closestBeacon = 9999999

      *#Each loop, get the distance to the nearest nav beacon
      for each $navBeacon in array $navBeacons
         $navBeacon.Distance = get distance between $navBeacon and [PLAYERSHIP]

         *#Store the closest beacon
         do if $closestBeacon > $navBeacon.Distance
            $closestBeacon = $navBeacon.Distance
      end 

      *#Determine if were getting hotter, or colder
      if $lastDistance < $closestBeacon
         display subtitle text: text='Hello World: Your getting hotter!' duration=1000 ms
      else
         display subtitle text: text='Hello World: Your getting colder!' duration=1000 ms
      end
  
      *#Store the current closest distance for the next loop
      $lastDistance = $closestBeacon

      = wait 500 ms
   end
endsub
```

> And there we have our hotter/colder display! now, onto the final event for this mission.

## The Ended Event ##
The final event for this mission is the Ended event. The Ended event is fired once the mission has been ended - Missions have 3 diffrent states that they can end in, Success, Failure or Ended. The Success and Failure cases are exactly what they seem, however the third case is the interesting one. A Mission can "End" neutrally, a neutral ending means the player hasen't done anything with the mission and as such the mission has ended silently either without the player knowing or with the player not caring.
For this tutorial mission, we only have "Success" and "Ended" cases, it cant fail in the traditional sense. _An exercise for the reader: Make the mission Fail if the player is within the same sector as the mission and is not the killer of the beacon._
```
* *******************************************
* ***********EVENT_MISSION_ENDED*************
* *******************************************
event_onMissionEnded:
   if $eventArgs == 'SUCCESS'
      $messageText = [THIS]->call script 'icdm.textdb.format': stringToFormat='Hello World! You Recieve ^Mission.Reward^!' lookupCacheTable=null Mission=$Mission
      = [THIS]-> call script 'icdm.mission.processrewardnotify' : targetMission=$Mission messageText=$messageText pctValue=100
   end

   *Dont forget to cleanup after your mission!
   $navBeacons = [THIS]-> call script 'icdm.mission.get.property' : targetMission=$Mission propertyName='navBeacons'
   for each $navBeacon in array $navBeacons
      do if $navBeacon->exists
         $navBeacon->destruct: show no explosion=[TRUE]
   end
endsub
```
And thats it! our Hello World mission is now complete. As you can see here we reward the player if the mission succeeded, but most importantly we **cleanup after ourselves** never leave mission objects in the game word after the mission is over if it can be prevented!

You may be wondering what the call to _icdm.textdb.format_ is for and the strange _Mission.Reward_ thing is in the message text, this is part of EMSML (EMS Markup Language) and will be automatically translated to the missions reward before sending the message to the player. More information on EMSML will be provided in future tutorials.

Be sure to follow onto the [Registering a Hello World Generator](EMS_Tut_Generator_Registration.md) tutorial to see the mission actually being started in the game world.
## The Complete Script ##
```
* # Hello, World

if $eventName == 'EVENT_SETUP'
   gosub event_Setup:
else if $eventName == 'EVENT_UPDATE'
   gosub event_Update:
else if $eventName == 'EVENT_ON_PLAYER_ENTER_AREA'
   gosub event_onPlayerEnterArea:
else if $eventName == 'EVENT_MISSION_ENDED'
   gosub event_onMissionEnded:
else if $eventName == 'SIGNAL_NAVBEACON_KILLED'
   gosub signal_NavBeaconKilled:
end

return null

* *******************************************
* ***************EVENT_SETUP*****************
* *******************************************
event_Setup:
   $missionSector = $Mission[1]
   $navBeaconCount = 3
   $navBeacons = array alloc: size=0
   while $navBeaconCount > 0
      dec $navBeaconCount
      $cNavBeacon.X = random value between -50000 and 50000
      $cNavBeacon.Y = random value between -50000 and 50000
      $cNavBeacon.Z = random value between -50000 and 50000
      $cNavBeacon = create ship: type={Neutral Race Navigational Beacon} owner=[Neutral Race] addto=$missionSector x=$cNavBeacon.X y=$cNavBeacon.Y z=$cNavBeacon.Z
      $cNavBeacon-> set relation against [PLAYERSHIP] to [Foe]
      $cNavBeacon-> set name to 'Hello, World!'
      = [THIS]-> call script 'icdm.mission.regsignal' : targetMission=$Mission targetObject=$cNavBeacon eventName='SIGNAL_NAVBEACON_KILLED' signal=[SIGNAL_KILLED]
      append $cNavBeacon to array $navBeacons
   end
   = [THIS]-> call script 'icdm.mission.set.property' : targetMission=$Mission propertyName='navBeacons' value=$navBeacons

   = [THIS]-> call script 'icdm.mission.set.autoupdate' : targetMission=$Mission autoUpdate=[TRUE] updateInterval=10
endsub

* *******************************************
* ***************EVENT_UPDATE****************
* *******************************************
event_Update:
   * #Fetch the missions sector
   $missionSector = $Mission[1]

   * #Fetch the Navigation Beacon array we defined earlier
   $navBeacons = [THIS]-> call script 'icdm.mission.get.property' : targetMission=$Mission propertyName='navBeacons'

   * #Set the players last distance to 0
   $lastDistance = 0

   while [TRUE]
      $missionState = $Mission[7]
      $newVersion = is a new script version available
      $playerSector = [PLAYERSHIP]-> get sector
      do if $missionState != 1 OR $newVersion OR $playerSector != $missionSector
         break

      * #Set the closest distance to something insanely large at fisrt!
      $closestBeacon = 9999999

      * #Each loop, get the distance to the nearest nav beacon
      for each $navBeacon in array $navBeacons
         $navBeacon.Distance = get distance between $navBeacon and [PLAYERSHIP]

         * #Store the closest beacon
         do if $closestBeacon > $navBeacon.Distance
            $closestBeacon = $navBeacon.Distance
      end

      * #Determine if were getting hotter, or colder
      if $lastDistance > $closestBeacon
         display subtitle text: text='Hello World: Your getting hotter!' duration=1000 ms
      else
         display subtitle text: text='Hello World: Your getting colder!' duration=1000 ms
      end

      * #Store the current closest distance for the next loop
      $lastDistance = $closestBeacon

      = wait 500 ms
   end
endsub

* *******************************************
* ********EVENT_ON_PLAYER_ENTER_AREA*********
* *******************************************
event_onPlayerEnterArea:
   return [FALSE]
endsub


* *******************************************
* ***********EVENT_MISSION_ENDED*************
* *******************************************
event_onMissionEnded:
   if $eventArgs == 'SUCCESS'
      $messageText = [THIS]->call script 'icdm.textdb.format': stringToFormat='Hello World! You Recieve ^Mission.Reward^!' lookupCacheTable=null Mission=$Mission
      = [THIS]-> call script 'icdm.mission.processrewardnotify' : targetMission=$Mission messageText=$messageText pctValue=100
   end

   *Dont forget to cleanup after your mission!
   $navBeacons = [THIS]-> call script 'icdm.mission.get.property' : targetMission=$Mission propertyName='navBeacons'
   for each $navBeacon in array $navBeacons
      do if $navBeacon->exists
         $navBeacon->destruct: show no explosion=[TRUE]
endsub


* *******************************************
* *********SIGNAL_NAVBEACON_KILLED***********
* *******************************************
signal_NavBeaconKilled:
   $killer = $eventArgs[1]
   if $killer == [PLAYERSHIP]
      = [THIS]-> call script 'icdm.mission.set.reward' : targetMission=$Mission rewardValue=100000 addMode=[TRUE]
      = [THIS]-> call script 'icdm.mission.end' : targetMission=$Mission Success=[TRUE] Failure=null
   else
      = [THIS]-> call script 'icdm.mission.end' : targetMission=$Mission Success=null Failure=null
   end
endsub

* *******************************************
return null
```