# The Phanon Corporation #

The Phanon Corporation is a competing faction.

## Hey, I remember this! ##

You may remember in the Egosoft forums that The Phanon Corporation was a script package that introduced a competing faction that bought traders, military, and stations in an effort to expand their empire.  It was mildly popular, bug reports were essentially non-existent, and performance was surprisingly good.

My goal in creating this plugin was to create some life in the Universe that carried on with out you, reacting to the game state. I also have a passion for performance, and paid close attention to the impact that this script might have on other factors in the Universe. I can avoid loop checks by storing pertinent information in arrays, and save script cycles by using priority sequence step timing (non-important tasks only checked once every 5 mins, etc.). Many years of testing went into this so far.

This AL Plugin can represent a challenge, especially in later levels, as The Phanon Coporation will steal trade opportunities, and actively hunt and destroy your ships and factories with M6 / M7 led fleets. As they gain more money, they will purchase capital ships to guard their HQ. Especially in later generations, the HQ can be difficult to destroy, as the sector will be well fortified.

If you want quick action, this script isn't for you; it was intended to be started at the same time as a player as a means to incite the player to get moving on creating his empire. Because if you don't, The Phanon Corporation will. And eventually, they will take over; but at a non-cheating pace. It can take just as much time for The Phanon Corporation's subsidiaries to build an empire as a player in the early generations. However, disturb them (kill their corvettes, cap their traders), and this progress will obviously slow.

It's been mentioned that the Phanon Corporation start out with a cash injection that is larger than the player's.  This is true.  If the Phanon started with a single M5 and 3,000 credits, it'd be a pretty anti-climactic game-play element.  Until I can implement multiple corporations, the Phanon Corporation will have to start out with an advantage.

## What's The Phanon Corporation Like in LU? ##

LU offers up a few changes over the original version.  Including the original, here's the features of the LU Phanon Corporation:

This plugin creates a new enemy faction, The Phanon Corporation, that is far more aggressive in its monopolization efforts than any existing known company (NNMC, Duke's, etc.)

  * Everything The Phanon Corporation buys, it pays for
  * It will not purchase anything if it doesn't have the funds required
  * Buys stations, traders, headquarters, fighters, capital ships
  * Maintains a proper fleet ratio (i.e. X number of m5s to m2s)
  * Corporation tasks include:
    * Trading
    * Search & destroy operations for enemy companies (that's you)
    * Station importers / Exporters
    * Sector guardian carriers
    * Sector guardian M8 bombers
    * TL Real Estate ship for placing stations
    * Rapid response carriers for station vandalism protection
  * The Phanon Corporation subsidiary earns money by trading, and a small allowance from the Phanon parent company.
  * The more it earns, the more it buys
  * 8 consecutive subsidiaries, increasing with buying power each generation (8 "levels", if you will).  The Phanon Corporation will automatically upgrade their corporation subsidiary when a certain level of military power has been acquired by the faction, or when their HQ is destroyed.
  * You will have an impact on their earning potential - kill a TS, and they have to buy a new one, and you decreased their trading income. They're just like you.
  * They will respond to their stations attacks if they have the military available
  * The Phanon Headquarters home sector is randomly chosen from a list of 13 Unknown and Pirate sectors. If you want spoilers, possible sectors are listed 8384-L044.xml. If the Phanon HQ is destroyed, a new sector will be chosen for the next subsidiary's HQ.
  * This script uses Race 1, so it might be incompatible with those scripts using Race 1.
  * Race 1 is set to neutral for all races. So shooting them will not effect your notoriety with anyone else.
  * The Phanon have no enemies except for you.
  * Performance has been increased over the original non-LU version due to the streamlining of a few antiquated processes.
  * The Phanon Corporation are slightly more economically viable in this version.