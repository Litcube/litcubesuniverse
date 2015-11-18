# Balance #

First off, I hate the word _balance_.  To me, it implies there's a perfect centre somewhere; as if there exists a magical nirvana for every game play system to achieve, and if it comes short, it's broken.  Also, it's not a feature, but whatever.

Everything has changed in LU.  Every missile, weapon, and ship in the game is not the same as you're used to in vanilla.  Nearly every item in the game has been balanced based off of targets, pivots, and their resulting formulas.  Very little of it was subject to individual conjecture.

## Balance Theory: Ships ##

![http://www.mediafire.com/convkey/1059/4wk8dmh8iw8931ifg.jpg](http://www.mediafire.com/convkey/1059/4wk8dmh8iw8931ifg.jpg)

I kept the classes the same.  As I've said in other forum posts, I'm not sold on there being any significant game play impact when it comes to new classes.  That doesn't mean they can't exist, but with the implementation of LU and the involved game play mechanics, I can't see it making a difference.

Ships in LU are spread out a bit in terms of capability.  The big ships, the capital ships, are juggernauts of destruction.  Most of them can fire massive volleys for quite some time before running out of juice.  Likewise, bigger ships can take significantly more damage.  Capital ship battles last a lot longer now.

If there was a class that I would flag as having changed most dramatically, it would be the M6.  They take more punishment, and are more capable and agile in general.

Ships cost more.  A lot more.  All ship costs are a result of the following formula:

=Formula.Balance.CombatAbility+Formula.Balance.Hauling+(1+Formula.Balance.Cargo/2)+Formula.Balance.Hull+Formula.Balance.Docking+Formula.Balance.SmallAddons

And each of these, of course, is broken down into smaller segments and further weightings.  For example:

Combat ability:
=(Formula.Balance.Shields\*Formula.Balance.Power\*Formula.Balance.Hull\*Formula.Balance.WeaponPower\*Formula.Balance.Agility)

Anyway, TMI.

## Balance Theory: Weapons ##

There's not much that resembles vanilla any more.  In LU, efficiency matters.  Your ships ability to sustain fire is going to be a little more stressed than it was in vanilla.  So while your ship may be able to install a HEPT that has a longer range, bigger boom, and faster bullets, you'll run out of juice 23% faster than the smaller alternative (just an example).  Maybe it's worth it.  Maybe it's not.  If you're building a carrier fleet, for example, you'll have to take efficiency into consideration.  If your MLCC carrier wing is set to take out fighters, you might want to opt for efficiency.  If they're going to run headlong into frigates, you may want to gamble that they'll take out the frigate in one pass, as opposed to going the long haul.  It's your choice based on the strategy you choose.


A few rules:

  * The larger the boom, the less efficient the weapon is.
  * Any weapon with the word "ion" in it has a higher shield damage to hull damage ratio than other weapons.
  * Bullet speed variation is large.  The enemy is more likely to hit you.  Your crazy strafing isn't going to work as well as it did.

Weapon cost was redone, and rounded to the nearest denomination of ware relval.  What the hell does that mean?  When you're producing a ware, your products should be low, and cycle time low.  If a relval doesn't divide properly with its resource's relval, products can be high, and cycle times high.  The end result is the same per hour average, but it's weird seeing 256 products per 234,384 minutes.

## Balance Theory: Missiles ##

Missiles in LU are faster, hit harder, and some are more durable against point defence weapons.  They will likely frustrate the hell out of you in early game.  This is intentional.  In the early game, you have no backup.  You suck.  You're in a single ship, and you want to take on the world.  Until you get backup, maybe get an M7 to protect you (it'll fire mosquitos at incoming missiles).

Rational: Missiles cost money.  So why would you use them if they did the same damage as your laser weapon?

You'll notice colours.  The icon colour matches the trail colour.  Colour represents their damage output.


_Note: These figures may not match the current version, the idea is to demonstrate the colour categories_
![http://www.mediafire.com/convkey/b313/m4qz5z2vj5d5lq4fg.jpg](http://www.mediafire.com/convkey/b313/m4qz5z2vj5d5lq4fg.jpg)



## Balance Theory: Factory Pricing ##

All player owned factories are a function of their respective product's price.  To a small exponent, the more the product costs, the more the factory costs.