# Dockware Manager #

Dockware Manager helps you organize the wares at your dock, and lets your various types of traders know what you want to keep, what you need to sell, and what to stock at the dock.  It also has features for easily single-click equipping your (hundreds)of ships through templates, and purchasing/equipping equipment upgrades and tuning upgrades.

There's a number of different traders you'll come to employ.  The Dockware Manager works with two of them; the Dock Agent and Freighter.  When you stock wares in your dock, as you would vanilla, the vanilla system automatically adds a ware entry to your dock, as you'll see in the _Info_ menu of the dock itself.  Even when you remove these wares, the entry still exists, even if you want it to go away.

The command can be accessed through the context menu on the dock itself.  Either through the sector map or the property menu.  When you launch it, you're presented with the first page _capacities_.  There's three pages in total: _capacities_, _sources_, _thresholds_.

The Dockware Manager allows the management of this system.  Through the three pages listed above, you'll be able to assign wares to the dock that you want to keep.

## Page: Capacities ##

![http://www.mediafire.com/convkey/7e5f/5oo205yvo35csz9fg.jpg](http://www.mediafire.com/convkey/7e5f/5oo205yvo35csz9fg.jpg)

The _capacities_ page's main function is to enable you to set the amount of wares you'd like to keep at your dock.  From here, you can also add wares that you're not yet tracking, and also add groups of wares that you don't have in your hold yet.

A fresh dock has no wares to track.  If you load wares from a docked ship to the dock, and then open Dockware Manager, you'll see that ware as _unassigned_.  If you select it, it will be added to the Dockware Manager in a predefined category such as weapons, shields, missile, or ship production components (components required by the HQ to produce ships).  If you click on an added ware, it will be removed from the dock (added to _unassigned_).  An assigned ware shows the current amount, capacity of the ware (to be followed by your trade ships), the percentage (stock over capacity), and the source of the ware, if set.

Highlighting an added ware and using arrow keys left and right, you're able to set the capacity of the ware.  This capacity is the amount to which your Dock Agent pilots or Freighter pilots will adhere to when stocking the dock.  Any amount **over** this capacity will be sold by your dock agent.  Your Freighters will also not ferry any more than your capacity from the wares sources.  More on this later.

If you want to set the capacity of an entire group of wares, first select the desired _ware group_.  Highlight the _set group capacity_ option.  Now use the arrows or keypad to set the desired capacity for the group (like the vanilla trade menu).  Hit enter, and the entire group of wares is added to your dockware manager at the chosen capacity.

## Page: Sources ##

![http://www.mediafire.com/convkey/2f37/3ift757ud2477ihfg.jpg](http://www.mediafire.com/convkey/2f37/3ift757ud2477ihfg.jpg)

The _sources_ page allows you to set optional sources for your added wares.  You can have Freighters ferry wares from a source to your dock.  In order for your Freighter to know from where to ferry these wares, highlight the ware, and select its source.  In the above image, you'll see that Meatsteak Cahoonas has a source; it's set to Saturn CH 20 Meatsteak.  As that Saturn Complex hub pumps out Meatsteak Cahoonas, your freighter will bring them to the dock.

You can also set a source to _buy_.  This will tell your Dock Agent that these wares should be purchased.  The Dock Agent will respect the prices in your dock's _adjust station parameters_ menu.  Make sure your dock has the required funds for these purchases.

## Page: Thresholds ##

![http://www.mediafire.com/convkey/3d97/fgdrfyrgrm0185tfg.jpg](http://www.mediafire.com/convkey/3d97/fgdrfyrgrm0185tfg.jpg)

The _thresholds_ page allows you to set the minimum amount in stock at a source before the Freighter will bother going to grab stock.  In the image above, you'll see that High Energy Plasma Throwers are set to 10%.  The Freighter will only go for more when the source station (which happens to be another Saturn Complex Hub 20x) is at 10% capacity or higher.  This function was introduced to ensure slow producing stations don't make for unnecessary trade runs by your Freighters.

When a ware is set to _overstock_, Freighters will continue to stock the ware despite the capacity settings.  Additionally, Dock Agents will not sell wares set to _overstock_.


---


The top portion of the menu has other options that are helpful for outfitting your ships using all these wares you're stocking.

## Function: Order Licensing ##

![http://www.mediafire.com/convkey/bec8/4o285ppo0m7p1j2fg.jpg](http://www.mediafire.com/convkey/bec8/4o285ppo0m7p1j2fg.jpg)

From this menu, you can order equipment, software, and tunings.  Once purchased (green), you'll be able to equip ships with these upgrades through the _upgrade ship_ menu.  In the example image above, you can see that this dock has purchased Best Buys Locator, Cargo Bay Extension and Fight Command Software MK1, among others.  Docked ships can now have these wares installed from here.  Licenses are purchased on a per dock basis.

NOTE: Licences are specific to the dock at which they are purchased and are not transferable to other docks.

## Function: Template Outfit ##

![http://www.mediafire.com/convkey/6891/428j75ei66t6os0fg.jpg](http://www.mediafire.com/convkey/6891/428j75ei66t6os0fg.jpg)

This function will enable you to outfit ships with your previously stored templates using the Template Manager (see fuckstick).

**Template:**  Select the previously stored template you wish to use to equip the selected ships with.
**Filter Matching shiptype:**  Only show ships that match the shiptype in the selected template.
**Filter outfitted ships:**  Only show ships that have **not** been outfitted with the selected template.
**Hide from property menu when equipped:** An option that will set the ship to _hide from property menu_ to _yes_ once equipped with the template.
**Assign home and send:**  Selecting a station with this value switch will, upon equipping the ship, set that ship's home base and send it to the selected station.

**Ship List**

You'll see a list of ships here.  To equip a ship with the selected template, you just have to click it (or highlight and hit enter).  The list is colour coded:

**Green:**  It's ready to be outfitted with the selected template, you have all the wares required to outfit with the selected template.
**Blue:**  It's been equipped with the selected template.
**Yellow:**  This ship has all the wares as specified in the selected template, however, one of the configuration options doesn't match the template spec.  For example, turret commands, autojump, etc.
**White:**  Your dock doesn't have the required wares to equip this ship with the selected template.

Provided they are licensed by your dock, all upgrades such as software and tunings are purchased using dock funds at the time of equipping through this menu.

## Function: Upgrade Ship ##

![http://www.mediafire.com/convkey/d4c3/yfiyzweiyybai1rfg.jpg](http://www.mediafire.com/convkey/d4c3/yfiyzweiyybai1rfg.jpg)

As you've seen, through the _order licensing_ function, you're able to purchase licenses for this dock.  Using the _upgrade ship_ menu will allow you to install those wares onto your docked ships.  In the example image above, you'll see there's two ships docked.  The Nova is selected, and the menu shows that Remote System Control Software was just installed onto the ship.


## Dockware Manager & the MLCC ##

Note that a dock with the MLCC installed renders you unable to manipulate some functionality of the Dockware Manager.  This is very intentional.  The MLCC will automatically handle all wares through the Dockware Manager, though you do have the ability to assign sources to the automatically added wares.  See: [MLCC](Feature_MLCC.md)