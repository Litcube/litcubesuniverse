# Courier #
## Basics ##

The courier has the ability to follow through with a user set delivery list.  It has the capability to load and unload, with specified amounts of wares at any destination owned by you.  For ships with which the courier cannot dock, it will use a transporter device to both load and unload wares.  The task type "loop" is optional and can be put anywhere on the courier's list; however, any delivery items below the loop would never be executed.

The courier ignores certain errors that would stop other commands in their tracks.  For example, it ignores error -105, no wares available in cargo.  This is going to happen a lot with the courier, because you may also be transporting with the destination points.  Again, the emphasis is on the loop.  If there were no wares this time around, maybe next time.  Think of the courier as your galactic janitor and delivery man who just don't give a fuck.

Keep in mind it's not the courier's job to buy or sell; there are other software commands for that.  The courier is intended to fill gaps in your trade network when you need specific wares repeatedly (using the "loop" type) to keep up supply.

The courier requires Trade Command Mk 2

![http://www.mediafire.com/convkey/b7a1/jy1nanwapbij7c4fg.jpg](http://www.mediafire.com/convkey/b7a1/jy1nanwapbij7c4fg.jpg)

## Courier Tasks ##
Seven tasks can be added to a Courier's queue:

  1. **Load** - Transfers the set number of the selected ware from the set source to the Courier. If the set number of wares is not available, it will take whatever amount the source has and move on to the next task.
  1. **Fill** - Transfers wares from the source to the Courier until the cargo bay contains the set amount. If there are not enough wares in the source to reach this amount, the Courier will wait until there are. The next task will not begin until the Courier's cargo bay contains the set number of wares. If the Courier already has the set amount, this task will be skipped.
  1. **Unload** - Transfers the set number of the selected ware from the set Courier to the set destination. If the set number of wares is not available in the Courier's cargo bay, it will transfer as many as it has and move on to the next task.
  1. **Stock** - Transfers wares from the Courier to the set destination until the destination contains the set amount. If the set number of wares is not available in the Courier's cargo bay, it will transfer as many as it has and move on to the next task. If the destination already has the set amount or more than the set amount, this task will be skipped.
  1. **Maintain** - Transfers wares from the Courier to the set destination until the destination contains the set amount. If the set number of wares is not available in the Courier, it will transfer as many as it has and move on to the next instruction. If the destination has more than the set amount, the excess wares will be transferred to the Courier. If the destination already has the set amount, this task will be skipped.
  1. **Return Home** - Instructs the Courier to dock at it's homebase.
  1. **Loop** - Restarts the task queue from task #1. Note that any tasks listed after a loop task will never be done.