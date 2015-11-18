# Military Logistics Command Center #

The MLCC is a system providing you a whole suit of features that enable you to automate outfitting, fuelling, and carrying out predefined attack strategies.

To use the MLCC, you require a dock owned by you (There are two uniquely named shipyards for sale, one for smaller MLCC ships and one to dock larger ships).  You install the MLCC suite through the commands menu on the dock itself.  After that you're able to bring up the MLCC set up menu which is hotkey initiated.

## Dockware Manager Integration ##

The MLCC will handle your Dockware management from here on out.  The only wares that will be added to the Dockware Manager are wares your ships use.  Obviously ships have to be homebased to the MLCC dock in order for them to be managed (as with every other MLCC feature).  You still have the option for using sources within the Dockware Manager so that you can assign Freighters to ensure your MLCC dock is stocked for the dock's fleet.  See: [Dockware Manager](Feature_Dockware_Manager.md)

## Assitance ##

![http://www.mediafire.com/convkey/ad17/4dfxbvlejvt43jbfg.jpg](http://www.mediafire.com/convkey/ad17/4dfxbvlejvt43jbfg.jpg)

Calling for assistance is likely one of the first orders you'll issue your MLCC ships.  The command essentially calls your MLCC ships to assist you in battle and execute their orders.  The menu above shows a few options.  The first two items are rally options depicting the behaviour of how the MLCC ships will get to you.  The rest are sliders you can use to include or exclude the shiptypes from the assist call, which you'll need to set prior to hitting a rally option.

  * Rally: standard:  Ships will use normal autojump settings to get to you, jumping to the nearest available point
  * Rally: jump beacon: If your ship has a jump beacon on board, the MLCC ships will use it. The jump beacon doesn't need to be deployed. The resulting jump in creates a giant wall formation in front of your ship, evenly spaced out, and all facing the same direction as you are, ready and waiting for your go code.


## Functionality & Orders ##

Once you have an MLCC station, you will be able to set various rules for how your fleets are auto managed.  There's 4 parts:

  * Sorties
  * Ship Rules of Engagement
  * Hangars
  * Missile Rules of Engagement

In order for the MLCC to have any functionality at all, you'll need to have ships assigned to the MLCC.  The assigned ships are intended to be of class M6 or larger.  Fighter capability is intended to be in the form of carrier wings, which should be homebased to a carrier, and the carrier, in turn, homebased to the MLCC.

## Sortie ##

> A **Sortie** is a single command through the MLCC menu.

> When you run a sortie, all of your ships at MLCC stations (of which there can be many) and were assigned a YES to their Sortie config, will jump to handle complaints that were registered by your traders (the complaints department).  To see the complaints department, open the _player console_.

> They will be smart.  There's math involved to ensure they stand a very good chance of winning the combat they choose.  They will smart jump; if the enemy is headed toward a gate, they'll jump to the enemy's targeted gate to intercept.

## Configuration Menu ##

The main configuration window is as follows:

![http://www.mediafire.com/convkey/c70b/iywkp8vgwuhok72fg.jpg](http://www.mediafire.com/convkey/c70b/iywkp8vgwuhok72fg.jpg)

It fields the configuration of ship rules of engagement and  missile rules of engagement.  You can also view your hangar settings from here.


## Ship Rules of Engagement ##

![http://www.mediafire.com/convkey/d519/9s0za0dsbr8nlc0fg.jpg](http://www.mediafire.com/convkey/d519/9s0za0dsbr8nlc0fg.jpg)

> Any ship **type** that has a homebase set to an MLCC enabled dock will show up in this menu. Here, you can configure 4 stages of orders.  The stages are just the order in which they act on those order.  Each stage can be assigned an order of:  Assault, Carrier, Retreat, Bomber, Escort.

> Each of those orders has config options.  For example assault: only engage fighters, or only engage capital ships.  Or for the carrier order, how many per wing to attack, and what to attack, how many losses can this ship type incur before retreating.

> For example (as per image above):
  * **Heavy Centaur Prototype:**
  * Order 1: Assault, Capitals
  * Order 2: Assault Fighters
  * Order 3: Assault, Capitals
  * Order 4: Protect Me

Here's another example config we'll reference shortly:

![http://www.mediafire.com/convkey/93c7/ir8jyvrcncwv5awfg.jpg](http://www.mediafire.com/convkey/93c7/ir8jyvrcncwv5awfg.jpg)

> Scenario for above config: You're in an OCV sector.  There's about 60 enemy ships.  You are alone.  But you have your fleet stationed at your MLCC docks fuelled and ready.  You hit a hotkey that launches an MLCC beacon (set in controls menu, interface).  Your MLCC ships know what that means: they jump to you immediately.  But not in a large mass.  In an organized wall facing your direction (that took a lot of math).

> The recent arrivals will wait in this wall formation until you give to go code.  You wait for the right moment to unleash hell (initiate your carefully crafted orders).

> You hit the MLCC GO Code (set in controls menu, interface).  Your ships launch into action, all executing your pre-coded orders.

> For example, your 16 Heavy Centaur Prototypes set in the example above will immediately start searching for Capital ships (order 1).  When none are left, they will attack fighters (order 2).  Then they will attack capitals again (order 3), in case any stragglers show up in scanner range.  They then will fly to you, and protect your ship (order 4).

> On MLCC Go Code, your Emeus ships as configured above will immediately launch all carried fighters.  Once all are launched, the fighters will go into a follow pattern, following their mothership until given further orders.  The carrier, meanwhile, is looking for _fighters_ as configured.  The carrier will b-line for the nearest enemy fighter.  Once within _intercept range_, the carrier will send wings of the task force size to intercept any fighters this way as long as there's an enemy within _intercept range_.

> If an enemy comes within _proximity protection range_ of the carrier, all fighters abandon orders and attack the closest object.  This can be turned off with _proximity protection_ set to _no_.

> If the carrier in this example loses 30% of its starting fighters as set in the _casualty tolerance_, the carrier will recall all remaining fighters and retreat.

> A few other notes on tasks:

> The _bomber task_ is essentially a turret configuration.  The bomber task is only valid for missile boat ships.  Set the turrets here, and when the ship jumps in, those turrets will be set.  It can be beneficial to set one turret as missiles only, as that turret command will protect your entire fleet from enemy missile attacks.  The monitor target and monitor range essentially tells the bomber to fly to the nearest target of that class at a distance of the range to play "keep away".

> The _escort_ task will tell ships of this type that have jumped in to escort a random _escort class_ ship in the fleet.  Multiple escorts of the same type will spread out evenly between leaders.  For example, if you have 2 M7s in the fleet, and you set 13 Centaurs to escort M7s, when the go code is launched, your Centaurs will each find an M7, and the result will be 6 Centaurs escorting one of the M7s, and 7 escorting the other.

## Hangars ##

> In our scenario above, you also had an Emeus, a nimble Teladi carrier ship with a hangar will of 22 Asps that each were equipped with IREs, 5MJ shields, and Wildfire missiles.  As you can see from the configuration image above, that Emeus had its hangar settings set to Air To Air Asp (a template made by you) and Otas McCallum Shipyard (your dock).  Your template looks like this in the _Template Manager_:

![http://www.mediafire.com/convkey/18f7/mopr94oh93j5n75fg.jpg](http://www.mediafire.com/convkey/18f7/mopr94oh93j5n75fg.jpg)

> When the fight was over (you won), the Emeus's Order 4 was to retreat.  Which it did.  It had lost 8 Asps in the battle.  When it jumps back to its home MLCC, it will know what its losses were, and 8 lost ships in the set hangar that _exactly_ match the asp configuration template of IREs, 5MJ shields, and wildfire missile, will fly to your Emeus, dock, and set their new homebase (to the carrier) automatically.  Your Emeus will then do what all other MLCC ships do now after retreating, they will dock, refuel, and reload all wares required which should be at their MLCC dock (see: [Feature\_Dockware\_Manager](Feature_Dockware_Manager.md)), which will include energy cells, missiles, or jump drive cores which may have been spent in the previous battle if this Emeus was unlucky (jump drive cores to be mentioned later).

> The hangar in question is a station that really does nothing but station fighter wings. It is referenced in the MLCC menu in the shiptype config (as per the Emus config example image above). The hangar section of the MLCC menu is basically a list of two fields:

  * What hanger?
  * What ships are stored here?

> The first field is simply a station where your fighters are docked, and for obvious reasons, it's a good idea to have the hangar in the same safe sector that your carrier's MLCC is setup.  The latter field is a Template entry. The ships in this hangar are probably going to be labelled _Reserve_ (which would have been done when you mass equipped them at a dock, see: [Feature\_Dockware\_Manager](Feature_Dockware_Manager.md)).
> Templates are set in the Template Manager.

## Missile Rules of Engagement (RoE): ##

![http://www.mediafire.com/convkey/3a02/51yh7x324b44dtkfg.jpg](http://www.mediafire.com/convkey/3a02/51yh7x324b44dtkfg.jpg)

> I found vanilla missile engagement lame.  So if a fighter's carrier is an MLCC ship it will use the missile ROE rules that you setup in the MLCC main menu.  It's important to note that these rules will only effect ships that call an MLCC home.  In the case of fighters, which don't directly call an MLCC home, will do so if their carrier calls an MLCC dock home.

> As you can see from the above image, the missile rules are basically as follows:
> > Missile Type
> > > Target Type
> > > > Range
> > > > Fire Rate


> With our Air to Air Asps example above, we'd need a quick missile.  Those 16 Wildfires would do. So we go into our MLCC main menu, and Add a new missile ROE.  The first field being the ship type that follows this rule.  We'd use the filters on the main configuration menu, maker race (Split), then class (M4), then select Asp. and hit "New" in the Missile ROE section.

> The Missile RoE for all Asps now shows.  We'll add the wildfire missile, because that's what we'll be using.

> Now we have to set what type of targets the wildfire should fire at.

> Add fighters.  Set the range to between 1,500m and 8,000m.  Frequency 80%.

> Add M2 to the wildfire (for lulz), set range to between to 10,000m and 25,000m.  Frequency 20%

> So now when our asps are in the field, if they see fighters, there's an 80% chance every 5 seconds they will fire a wildfire at a nearby enemy fighter if it is within the range of between 1,500m and 8,000m.

> Also, if there's an M2 within 10,000m and 25,000m, it will fire a wildfire 20% of the time.

> You can add as many target RoEs, per as many missiles, per as many ship types as you want.

> I found Discoverers loaded with fireflies attacking an M2 to be devastating.  Expensive as hell, but devastating.