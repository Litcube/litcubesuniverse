# Anatomy of a Mission #
There are 4 potential parts to every mission, a brief overview is given here, more details are provided in the tutorials that follow.

  * ## Generator ##
> > _(Script Name: icdm.module.[[ModuleName](ModuleName.md)].generator)_


> A Generator, as the name suggests - is the part responsible for creation of missions, it can accomplish its goal in one of two ways:

> The Generator can act as an AL with a timed update, the update can be used to run scans of the game state to determine whether a mission should be created. Using actual AL's for this job is not reccomended, Generators should be prefered over AL's for reasons that will be outlined in the articles [Custom Events](EMS_Tut_CustomEvents.md) and [Script Event List](EMS_Tut_Events.md).

> The Generator can also receive global game signals, EMS events, IceCore System events and Custom events (which we will cover later) - from now on all forms of signal or event will simply be referred to as "events".

  * ## Mission Script ##
> > _(Script Name: icdm.module.[[ModuleName](ModuleName.md)].missionscript)_


> The mission script is the actual code that runs your mission, if your mission has more then one stage it is quite possible that you could have more then one mission script for your missions.

> Mission scripts function in much the same was as Generators do, however instead of handling global signals, missions handle Local signals on objects and special events from the EMS core for monitoring what the player is doing.

> Missions exist as instances, each mission is contained within its own mission array (see [Array Docs](EMS_ArrayDocs.md) for the structure) - the mission script is always called with an mission instance as its first argument. More information about script arguments be found in the article [Script Structure](EMS_Tut_Structure.md).

  * ## Setup Script ##
> > _(Script Name: setup.icdm.module.[[ModuleName](ModuleName.md)])_


> An setup script is used to register your mission generators with the EMS core, usually this is all the setup script does as any further intiliasion should be performed within the Generator on EVENT\_SETUP or EVENT\_ON\_SAVE\_LOADED. See the [Script Event List](EMS_Tut_Events.md) for more information on events.

  * ## Init Script ##
> > _(Script Name: init.icdm.module.[[ModuleName](ModuleName.md)])_


> Init scripts are an often underutilized feature of the X scripting engine, these scripts are called before the the job engine starts up and before the player ships is created (providing this is a new game load). They are always called before setup scripts. If there is anything that must be done before any setup scripts are called then it should be done in an init script. Init scripts also help you overcome the problem of "Well, what if this setup script isn't run before mine?".