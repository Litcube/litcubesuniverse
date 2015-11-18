# Script Structure #
Both Generators and Mission Scripts share a common structure, Because EMS is based around event driven programming, each event received by the script is dispatched to a subroutine.

The general structure of the scripts are as follows:

Arguments:
  * Instance of an Mission/Generator
  * String representing the Event Name
  * Variable with the Event args
```

if $eventName == 'Event1'
  gosub Event_1
else if $eventName == 'Event2'
  gosub Event_2
end

return null
*******************
Event_1:

endsub
*******************
Event_2:

endsub
```
## Template Code ##
Below are templates for the creation of Generators or Mission Scripts.
For more information about each of the events, see the [Script Event List](EMS_Tut_Events.md).
### Generator ###
  * Generator : Generator Instance Array
  * eventName : String (Event Name)
  * eventArgs : Variable (Event Arguments)
```
* This is a template for a mission generator

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
endsub

* *******************************************
* ***************EVENT_UPDATE****************
* *******************************************
event_Update:
endsub

* *******************************************
* ***********EVENT_ON_SAVE_LOADED************
* *******************************************
event_onSaveLoaded:
endsub

* *******************************************
* *******EVENT_ON_PLAYER_CHANGESECTOR********
* *******************************************
event_onPlayerChangeSector:
endsub

* *******************************************
return null
```

### Mission Script ###
Arguments:
  * Mission   : Mission Instance Array
  * eventName : String (Event Name)
  * eventArgs : Variable (Event Arguments)
```
* This is a template for a mission script

if $eventName == 'EVENT_SETUP'
  gosub event_Setup:
else if $eventName == 'EVENT_UPDATE'
  gosub event_Update:
else if $eventName == 'EVENT_ON_PLAYER_ENTER_AREA'
  gosub event_onPlayerEnterArea:
else if $eventName == 'EVENT_ON_PLAYER_LEAVE_AREA'
  gosub event_onPlayerLeaveArea:
else if $eventName == 'EVENT_PRIMARYOBJECT_LOST'
  gosub event_onPrimaryObjectLost:
else if $eventName == 'EVENT_PRIMARYOBJECT_CHANGESECTOR'
  gosub event_onPrimaryObjectChangeSector:
else if $eventName == 'EVENT_ON_PLAYER_CHANGESECTOR'
  gosub even_onPlayerChangeSector:
else if $eventName == 'EVENT_MISSION_ENDED'
  gosub event_onMissionEnded:
else if $eventName == 'EVENT_ON_MISSION_AMALGAMATED'
  gosub event_onMissionAmalgamated:
end

return null

* *******************************************
* ***************EVENT_SETUP*****************
* *******************************************
event_Setup:
endsub

* *******************************************
* ***************EVENT_UPDATE****************
* *******************************************
event_Update:
endsub

* *******************************************
* ********EVENT_ON_PLAYER_ENTER_AREA*********
* *******************************************
event_onPlayerEnterArea:
return [TRUE]
endsub

* *******************************************
* ********EVENT_ON_PLAYER_LEAVE_AREA*********
* *******************************************
event_onPlayerLeaveArea:
endsub

* *******************************************
* *********EVENT_PRIMARYOBJECT_LOST**********
* *******************************************
event_onPrimaryObjectLost:
endsub

* *******************************************
* *****EVENT_PRIMARYOBJECT_CHANGESECTOR******
* *******************************************
event_onPrimaryObjectChangeSector:
endsub

* *******************************************
* *******EVENT_ON_PLAYER_CHANGESECTOR********
* *******************************************
even_onPlayerChangeSector:
endsub

* *******************************************
* ***********EVENT_MISSION_ENDED*************
* *******************************************
event_onMissionEnded:
endsub

* *******************************************
* *******EVENT_ON_MISSION_AMALGAMATED********
* *******************************************
event_onMissionAmalgamated:
endsub

* *******************************************
return null
```