# Auto Updates #

Both generators and mission scripts support auto updates, these updates function in a very similar way as to AL updates, with one major difference: EMS Auto-Updates will never, ever, result in an update pileup the same way AL's pileup.

This is achieved via a new script command in LU that is able to check to see if a task is running with a specific PID, while that task is running, a new one will not begin.

In order to toggle auto updates for your generators or mission scripts, use the appropriate script:

```
= [THIS]->call script 'icdm.generator.set.autoupdate': targetGenerator=$Generator autoUpdate=[Boolean] updateInterval=60
```
```
= [THIS]->call script 'icdm.mission.set.autoupdate': targetMission=$Mission autoUpdate=[Boolean] updateInterval=60
```

# Update Resolution #

The update system has an unreliable resolution, this means that even tho you request an update every 60 seconds, more time may pass before an update is received, however at least 60 seconds will always pass.

The minimum update resolution is 10 seconds, meaning that update intervals of less then 10 seconds are not possible. The maximum update resolution is equal to (10 + ($ActiveMissionCount / 4)) seconds. Given an average of 20 active missions with updates enabled that is a resolution minimum resolution of 15 seconds.

The reason the resolution on the timer is so lax is for performance reasons, if you require a timer with more precise resolution, see the below heading.

# Looping and Waits #

Because of how EMS performs its updates, you are free to run loops within the update that last for the entire lifetime of the mission. You are free to wait as often as you like and take as long as you like within your missions update call.

If the update resolutions above are not good enough for your mission, say for example you absolutely require and update once every second, you are free to do the following:

_(however please also take into account the performance effect this may have if allot of your missions with updates like this are started!)_

```
while [TRUE]
  $missionState = $Mission[7]
  $newVersion = is a new script version available
  do if $missionState != 1 or $newVersion
     break

  * Your update stuff

  = wait 1000 ms
end
```

In the above code block, $Mission[[7](7.md)] references the missions "state" (see [Array Docs](EMS_ArrayDocs.md) for more information about mission array indexes) - there are 4 possible values:
  * 1 - Active
  * 2 - Success
  * 3 - Failed
  * 4 - Ended

So long as the mission is in the Active(1) state, the mission is running and we can continue our loop. We also break in case of a new version so that if you have an error in your loop you can update the script and have EMS automatically restart your update loop.