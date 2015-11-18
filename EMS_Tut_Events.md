# Event Information #
Events are categorized into one of three category's:
  * <font color='red'>Real Time</font>
> > Real Time events must return **as fast as possible** without **any waits**, all loops **must be written ensure they end** - Real Time events are usually thoes that originate from Signals, as such they cannot have any waits or you will create errors in the engine and save-game that may be unrecoverable.

  * <font color='blue'>Synchronous</font>
> > Synchronous events are, as the name suggests, called synchronously. They are allowed to use waits but any loops should be written to ensure they exit, preferably as soon as possible. Synchronous calls should limit waits as much as possible to prevent the calling task from waiting too long.

  * <font color='green'>Asynchronous</font>
> > Asynchronous events are started Asynchronously meaning they do not have a calling task that can get held up, Asynchronous events can use loops, waits and can otherwise run forever, tho unless its an UPDATE event, it is generally recommended to exit the event within a reasonable amount of time.

# Generator Events #

  * EVENT\_SETUP _(_<font color='red'>Real Time</font>)_> > The SETUP Event is fired only once, when a generator is registered to the system for the very first time. Do not confuse this event with the SAVE\_LOADED event._

  * EVENT\_UPDATE _(_<font color='green'>Asynchronous</font>)_> > The UPDATE event is fired for each update interval, more information about updates is available in the article [Auto-Updates, Looping and Waits](EMS_Tut_Updates.md)._

  * EVENT\_ON\_SAVE\_LOADED _(_<font color='red'>Real Time</font>)_> > The SAVE\_LOADED event is fired each time the player loads a savegame, including the very first time the game starts._

  * EVENT\_ON\_PLAYER\_CHANGESECTOR _(_<font color='red'>Real Time</font>)_> > The PLAYER\_CHANGESECTOR event is called every time the_PLAYERSHIP_changes sector._

# Mission Script Events #

  * EVENT\_SETUP _(_<font color='green'>Asynchronous</font>)_> > The SETUP event is fired whenever the mission is started, the SETUP event can also be called if the mission script of the mission has changed via the use of icdm.mission.set.missionscript._

  * EVENT\_UPDATE _(_<font color='green'>Asynchronous</font>)_> > The UPDATE event is fired for each update interval, more information about updates is available in the article [Auto-Updates, Looping and Waits](EMS_Tut_Updates.md)._

  * EVENT\_ON\_PLAYER\_ENTER\_AREA _(_<font color='blue'>Synchronous</font>)_* Return Value: TRUE = Show Mission On Overlay | FALSE = Inverse True
> > The PLAYER\_ENTER\_AREA event is fired when the player enters the missions sphere of influence, if the return value is TRUE, the mission will be shown on the right side of the screen overlay._

  * EVENT\_ON\_PLAYER\_LEAVE\_AREA _(_<font color='blue'>Synchronous</font>)_> > The PLAYER\_LEAVE\_AREA is fired when the player leaves the missions sphere of influence - if the mission was on the right screen overlay, it will now be removed regardless of return value._

  * EVENT\_ON\_PLAYER\_CHANGESECTOR _(_<font color='red'>Real Time</font>)_* Event Args: Target Sector
> > The PLAYER\_CHANGESECTOR event is fired whenever the_PLAYERSHIP_changes sector._

  * EVENT\_MISSION\_ENDED _(_<font color='blue'>Synchronous</font>)_* Event Args: String ('SUCCESS' | 'FAIL' | 'ENDED')
> > The MISSION\_ENDED event is fired whenever icdm.mission.end is called, the event argument contains the ending case of whether the mission failed, succeed or ended neutrally._

  * EVENT\_PRIMARYOBJECT\_LOST _(_<font color='red'>Real Time</font>)_* Event Args: ARRAY
      * [[0](0.md)] String ('KILLED' | 'BAILED')
      * [[1](1.md)] Primary Object
      * [[2](2.md)] Killer/Attacker
> > The PRIMARYOBJECT\_LOST event is fired whenever the missions primary object either bails, or is killed. Ideally you should select a new primary object (or primary location) or end the mission if no primary object could be determined. While missions can exist without primary objects, the player will only know of there existence via the missions sphere of influence, which extends from the primary objects location._

  * EVENT\_PRIMARYOBJECT\_CHANGESECTOR _(_<font color='red'>Real Time</font>)_* Event Args: Target Sector
> > The PRIMARYOBJECT\_CHANGESECTOR event is fired whenever the mission_Primary Object_switches sector._

  * EVENT\_ON\_MISSION\_AMALGAMATED _(_<font color='red'>Real Time</font>)