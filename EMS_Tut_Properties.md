# Mission Properties #

Missions in EMS can support local variables in much the same way as [Other Objects](ScriptEngine_Feature_LocalVariables.md) in the game, however because EMS missions are just arrays, you must use the two following script to read/write to them:

Reading Mission Local Variables:
```
$Value = [THIS]-> call script 'icdm.mission.get.property' : targetMission=$Mission propertyName='myPropertyName'
```

Writing Mission Local Variables:
```
= [THIS]->call script 'icdm.mission.set.property' : targetMission=$Mission propertyName='myPropertyName' value=$myPropertyValue
```

You can use mission properties to store anything you like, mission properties can also be read by the EMS Markup Language that is used when formating mission texts, more information about EMSML can be found in the [EMS Markup Language](EMS_Tut_EMSML.md) article.