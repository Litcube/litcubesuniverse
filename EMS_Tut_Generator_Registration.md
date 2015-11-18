# Hello->getWorld().Generate() #

In this tutorial we are going to use the mission script we are going to write a simple generator for the mission script we created in the last tutorial _(which we named "icdm.module.tutorial.missionscript")_

## Setting up the Generator Script ##
Similar to the last tutorial - we need to create the Generator script from the template that EMS provides. Simply open up the _"icdm.module.template.generator"_ script and save it as whatever you wish to name the mission script, just like before i recommend leaving most of the name intact and simply changing the module name like so: _"icdm.module.**tutorial**.generator.xml"_

## Creating the Setup Script ##
You can use any setup script name you like, but as usual i recommend following a unified format: For the tutorial we are going to create the setup script called _"setup.icdm.module.**tutorial**"_.

The setup script is required to register the generator, and in this tutorial it is literally a one liner. Here is the setup script:

```
= [THIS]-> call script 'icdm.generator.register' : eventScript='icdm.module.tutorial.generator'
```

## The Generation Code ##
This generator is very simple - when the player enters the sector "Home of Light" the mission will be started.

```
* *******************************************
* *******EVENT_ON_PLAYER_CHANGESECTOR********
* *******************************************
event_onPlayerChangeSector:
   if $eventArgs == [Home of Light]
      * #Check to see if the sector has a mission lock
      if not [THIS]->call script 'icdm.lib.object.getmissionlock': Object=$eventArgs lockCode='MTYPE_NAVBEACON_TUTORIAL'
         * #Start the mission
         $Mission = [THIS]-> call script 'icdm.mission.start' : missionScript='icdm.module.tutorial.missionscript' primaryObject=$eventArgs missionRace=null requiredRaceRep=0
         * #Apply a lock to the sector so that we can only start ONE mission at once
         = [THIS]->call script 'icdm.lib.object.setmissionlock': Object=$eventArgs targetMission=$Mission lockCode='MTYPE_NAVBEACON_TUTORIAL'
      end
   end
endsub
```
You may notice the Mission Lock calls in there, they will be touched on in detail in the article [Mission Locks](EMS_Tut_Locks.md) - however for now the basic understanding should be straightforward. The object mission lock scripts allow you to prevent the creation of more then one mission in refrence to a spesific object - in this case, only one mission is allowed to start in "Home of Light".

## The Final Generator Code ##
With the mission script, setup script and generator all created in your game, you should now be able to go to home of light - find one of the beacons, and destroy it for a 100,000 Cr reward!.

```
if $eventName == 'EVENT_SETUP'
  gosub event_Setup:
else if $eventName == 'EVENT_UPDATE'
  gosub event_Update:
else if $eventName == 'EVENT_ON_SAVE_LOADED'
  gosub event_onSaveLoaded:
else if $eventName == 'EVENT_ON_PLAYER_CHANGESECTOR'
  gosub event_onPlayerChangeSector:
end

return null


* *******************************************
* ****************EVENT_SETUP****************
* *******************************************
event_Setup:
 *# The SETUP event is fired once and only ONCE when the generator is first registered with the system.
 *# Use this for any one time code that needs executing
endsub

* *******************************************
* ***************EVENT_UPDATE****************
* *******************************************
event_Update:
 *# Just like Mission Scripts, Generators can be registered for auto updates.
endsub

* *******************************************
* ***********EVENT_ON_SAVE_LOADED************
* *******************************************
event_onSaveLoaded:
 *# This event is fired every time a savegame is loaded.
endsub

* *******************************************
* *******EVENT_ON_PLAYER_CHANGESECTOR********
* *******************************************
event_onPlayerChangeSector:
   *# This event is fired every time the [PLAYERSHIP] changes sector.
   if $eventArgs == [Home of Light]
      * #Check to see if the sector has a mission lock
      if not [THIS]->call script 'icdm.lib.object.getmissionlock': Object=$eventArgs lockCode='MTYPE_NAVBEACON_TUTORIAL'
         * #Start the mission
         $Mission = [THIS]-> call script 'icdm.mission.start' : missionScript='icdm.module.tutorial.missionscript' primaryObject=$eventArgs missionRace=null requiredRaceRep=0
         * #Apply a lock to the sector so that we can only start ONE mission at once
         = [THIS]->call script 'icdm.lib.object.setmissionlock': Object=$eventArgs targetMission=$Mission lockCode='MTYPE_NAVBEACON_TUTORIAL'
      end
   end
endsub

* *******************************************
return null
```