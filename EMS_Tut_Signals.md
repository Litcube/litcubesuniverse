# Signals #

Normally when writing missions and AL's for X, Signals are a heavily used feature of the games engine, in EMS this is no exception, However the way in which you use signals changes. EMS has special signal dispatching for Mission Scripts that hides the spesifics of the signals and allows you to get down to buisness with coding the actual mission rather then writing the signal framework.

Mission's only deal with Local signals on object, To deal with Global signals this is where generators come into play.

# Generator Global Signals #
Generators use global signals, because of the nature of global signals we dont have a nice encapsulated system like mission script do for local signals, but we do have a template script. Here is an example signal script from the SOS mission:

```
* Generic Global Signal Dispatcher for Mission Generators
$generator = [THIS]-> call script 'icdm.generator.find' : generatorGUID='icdm.module.sos.generator'
if $generator
  $eventArgs = create new array, arguments= [THIS], $arg1, $arg2, $arg3, $arg4, $arg5, $arg6, null, null
  = [THIS]->call script 'icdm.generator.fireevent': generatorTarget=$generator eventName=[SIGNAL_ATTACKED] eventArgs=$eventArgs
end
return null
```

As you can see here, we are simply encapsulating the signals arguments into an array and passing the signal onto the generator to be handled, in order to make your own signal scripts for generators you need only change two things in this code.

The First
> You must replace the name of the generator script to your own generator
```
$generator = [THIS]-> call script 'icdm.generator.find' : generatorGUID='icdm.module.sos.generator'
```


The Second
> Remember to change the signal shown here to the signal you are interested in.
```
= [THIS]->call script 'icdm.generator.fireevent': generatorTarget=$generator eventName=[SIGNAL_ATTACKED] eventArgs=$eventArgs
```

To make implementing generator signals easy, the script 'icdm.module.template.signal' provides this code in an easy to copy format, all you need do is change the 'template' in the script name to your module name and change the above information to complete your signal script.

After you have your signal script, it is simply a matter of registering it in your generator, here is an example from the SOS generator
```
* *******************************************
* ***********EVENT_ON_SAVE_LOADED************
* *******************************************
event_onSaveLoaded:
  global secondary signal map: remove signal=[SIGNAL_ATTACKED] race=null class=[TS] name='icdm.module.sos.sigattacked.ts'
  global secondary signal map: add signal=[SIGNAL_ATTACKED] race=null class=[TS] script='icdm.module.sos.sigattacked' prio=0 name='icdm.module.sos.sigattacked.ts'
endsub
```

You may be asking, why do you unregistered the signal and then register it? - this is a good habit to get into when dealing with global signals as the signal script gets cached into the save-game, if you make any changes to the signal script after its registered they wont be reflected until the signal is unregistered and re-registered.

After reading the below heading about Mission Script signals you may be wondering why the generator global signals are so convoluted to use. The answer is simple - Global signals have multiple diffrent states they can be in, signified by the "race" and "class" arguments provided to the register command. Because of this they are not easy to dispatch to the right places in the same way that local signals are and for the sake of performance signal dispatching for generators was not included.

# Mission Script Local Signals #

Missions use local signals, these signals can be very useful to track events in your mission. For the sake of this example were going to use a Nav Beacon, which we want to know when it has been destroyed. For this example we are going to assume that the Nav Beacon is not the missions primary object, as if it was the primary object of the mission we could simply track this via the use of the event EVENT\_ON\_PRIMARYOBJECT\_LOST.

The first step is to create the nav beacon and then register the signal to it. We will do this in our example mission script's EVENT\_SETUP event.
```
* *******************************************
* ***************EVENT_SETUP*****************
* *******************************************
event_Setup:
  $navBeacon = create ship: type=[Navigational Beacon} owner=[Neutral Race] addto=[Argon Prime] x=0 y=0 z=0
  = [THIS]->call script 'icdm.mission.regsignal': targetMission=$Mission targetObject=$navBeacon eventName='ON_NAVBEACON_DESTROYED' signal=[SIGNAL_KILLED]
endsub
```

And thats it! - Now, when our Nav Beacon is destroyed our mission will recieve the event 'ON\_NAVBEACON\_DESTROYED'. If you decide at a later point you no longer need this event, you can unregister it like so:

```
  = [THIS]->call script 'icdm.mission.unregsignal': targetMission=$Mission targetObject=$navBeacon signal=[SIGNAL_ATTACKED]
```

As a bonus, Mission Signals are automatically unregistered when the mission ends, meaning that you may never have to worry about unregistering the signal manually depending apon its purpose and your requirements.

This is a very simple yet powerful system which you can use to receive events based on game signals. The following signals are supported:

  * SIGNAL\_ATTACKED
  * SIGNAL\_CAPTURED
  * SIGNAL\_CHANGEDSECTOR
  * SIGNAL\_DOCKED
  * SIGNAL\_KILLED
  * SIGNAL\_SCANNED
  * SIGNAL\_SELLWARE
  * SIGNAL\_BUYWARE
  * SIGNAL\_LOADWARE
  * SIGNAL\_UNLOADWARE

# Signal $eventArgs #

When handling a signal, the $eventArgs script argument is set to an array, the array holds the arguments for the signal. $eventArgs[[0](0.md)] is always the relevant object for the signal and $eventArgs[[1](1.md)]+ is the standard arguments for the signal. For example with SIGNAL\_ATTAKCED, $eventArgs[[0](0.md)] would be the ship thats being attacked, and $eventArgs[[1](1.md)] is the ship thats attacking it.