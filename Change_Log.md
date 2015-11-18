# Change Log #

### Legend ###
  * 1 = Very minor
  * 2 = Minor
  * 3 = Average
  * 4 = Critical
  * 5 = Seriously Fucking Critical



---

# Version 1.5.2LU #
### July 5th, 2015 ###
  * **Code base: [Tapir](http://en.wikipedia.org/wiki/Tapir)**

  * (3) Fixed: Freighter debug spam
  * (2) Fixed: Omicron Channel SPPs required primary resources (map change)
  * (2) Fixed: Small errors in jobs file
  * (1) Fixed: Extraneous station info in SCH calculator sun efficiency display fixed

---

# Version 1.5.1LU #
### May 31, 2015 ###
  * **Code base: [Tapir](http://en.wikipedia.org/wiki/Tapir)**

  * (3) Fixed: Freighters would not pick up goods if homebase was overstocking and homebase was a trade dock
  * (2) Fixed: Station Agents could try and buy more resources than the station could hold
  * (2) Fixed: Unfucked repair laser sound

---

# Version 1.5.0LU #
### January 19, 2015 ###
  * **Code base: [Tapir](http://en.wikipedia.org/wiki/Tapir)**

  * (1) Fixed: Version display

---

# Version 1.4.9LU #
### January 18, 2015 ###
  * **Code base: [Tapir](http://en.wikipedia.org/wiki/Tapir)**

  * (5) Fixed: Packing error, accidentally included an export file

---

# Version 1.4.8LU #
### January 17, 2015 ###
  * **Code base: [Tapir](http://en.wikipedia.org/wiki/Tapir)**

  * (3) Fixed: When training all skills, fighting skill would not train correctly
  * (3) Fixed: If other 3 marine skills were at 100, no option for fight training was available
  * (3) Fixed: Marine skill display on property menu was out of order
  * (3) Fixed: Non-Commonwealth race sectors taken over by OCV were sending messages
  * (3) Fixed: Ship Compendium now displays OTAS notoriety requirements correctly
  * (3) Fixed: Freighters were not loading goods sometimes
  * (3) Fixed: Upgrading multiple ships would incorrectly record spent money on a ship's trade report when buying tunings
  * (-) Changed: Player ships now auto-fuel energy cells from player owned stations even if the energy is a secondary resource
  * (-) Changed: 'Cmdwing action many calls this' spam should now be removed
  * (-) Changed: Increased normal kill notoriety increases by double
  * (-) Upgraded: New reference object script constants for MSCI: NULL, PLAYERSHIP

---

# Version 1.4.7LU #
### November 14, 2014 ###
  * **Code base: [Hirola](http://en.wikipedia.org/wiki/Hirola)**

  * (5) Fixed: Packing error

---

# Version 1.4.6LU #
### November 14, 2014 ###
  * **Code base: [Hirola](http://en.wikipedia.org/wiki/Hirola)**

  * (3) Fixed: Lag could occur when a big ship was swarmed, had emergency jump activated, but no means to do jump
  * (3) Fixed: Trade reports not generated correctly when purchasing new ships and equipping
  * (3) Fixed: Trade reports not generated when a station was selling to NPCs
  * (3) Fixed: Trade report was screwing up on a Dock Agents bulk sell and also Sell Spare Equipment command
  * (2) Fixed: Thank you on killed messages now come from the sector owner as opposed to vanilla style (some random dock owner)
  * (-) Changed: FLC nerfed; see [FLC](Feature_FLC.md)
  * (-) Upgraded: Marines now show stats when viewed, as opposed to just stars
  * (-) Upgraded: Fighting ability added to marine view in dock trade menu
  * (-) Upgraded: Marine stats order displayed properly in dock menu (matches trade window)
  * (-) Upgraded: Marine fight training added to docks (removed TL combat training command)
  * (-) Upgraded: Property menu, personnel tab now shows percent completion of marine training

---

# Version 1.4.5LU #
### November 8, 2014 ###
  * **Code base: [Dugong](http://en.wikipedia.org/wiki/Dugong)**

  * (5) Fixed: God damnit

---

# Version 1.4.4LU #
### November 8, 2014 ###
  * **Code base: Dugong**

  * (5) Fixed: Plutarch Tractor System was destroying roids

---

# Version 1.4.3LU #
### November 8, 2014 ###
  * **Code base: [Dugong](http://en.wikipedia.org/wiki/Dugong)**

  * (4) Fixed: Wing ships jumping in can get phantomed at sector center
  * (3) Fixed: Odd and rare courier menu bug showing deploy satellites was a typo
  * (3) Fixed: Miners will not longer error out when only having one Mobile Drilling System installed
  * (3) Fixed: SCHs automatic operation on remove could fuck up adding resources back to asteroids
  * (2) Fixed: Order strings now work properly for miners
  * (2) Fixed: Phanon HQ name wasn't changing between subsidiaries
  * (-) Upgraded: Plutarch Tractor System now selects the next closest source asteroid of same type ready for engage when compacting
  * (-) Changed: Added more asteroids to the map (map change)
  * (-) Changed: Plutarch Tractor System requires more resources

---

# Version 1.4.2LU #
### October 31, 2014 ###
  * **Code base: [Dugong](http://en.wikipedia.org/wiki/Dugong)**

  * (4) Fixed: Tractor Asteroid was creating debris instead of Asteroid
  * (2) Fixed: Pirate miner escorts weren't pretending they weren't pirates as well as their leader
  * (2) Fixed: Keris, Fighter Drone MK 2, now have reputation requirements
  * (2) Fixed: Mining Outposts were not supposed to be equipment docks
  * (2) Fixed: SCH Disengage error message should tell you TL isn't docked, not that there is null cargo available
  * (2) Fixed: Dockware Manager set group capacity would add weird capacity values to wares that were unassigned
  * (2) Fixed: Dockware Manager now filters complexed undockable stations for sources
  * (-) Changed: Tractor Asteroid command renamed to Plutarch Tractor System
  * (-) Changed: Betty was drunk again, so Avarice was renamed Guiding Star
  * (-) Changed: Deploy Satellite command now has proper error message for transport class issue
  * (-) Changed: Missile, Laser fabs reputations all require + 1 rank than their product

---

# Version 1.4.1LU #
### October 25th, 2014 ###
  * **Code base: [Dugong](http://en.wikipedia.org/wiki/Dugong)**

  * (4) Fixed: Keris was not installing plasma gun
  * (4) Fixed: Trade reports run on ships were cancelling ship orders (task 0, DERP)
  * (3) Fixed: Space suit was not equipping repair laser
  * (3) Fixed: Escort: Attack Same will now attack stations if leader has target set to a station
  * (3) Fixed: Emergency Jump now works on wings, temporarily removed until the emergency jump is complete.
  * (3) Fixed: Global ship renaming proposed changes array was reversed (st rename bug with different ship types)
  * (3) Fixed: Headquarters now requires notoriety; woops
  * (-) Changed: UTs now refuel before buy and sell if station is beyond jump fuel range, or jump fuel is less than 8 jumps
  * (-) Changed: Increased TS miner rotation agility
  * (-) Changed: OCV's three resources changed to Red Crystal, Orange Mineral, Purple Mineral
  * (-) Changed:  _get asteroid array from sector_ now only returns asteroids of type 0 (the mine placement asteroids, not debris)
  * (-) Changed: Balanced Dockware Manager licensing
  * (-) Upgraded:  New script command _get debris array from sector_

---

# Version 1.4.0LU #
### October 24th, 2014 ###
  * **Code base: [Jellyfish](http://en.wikipedia.org/wiki/Jellyfish)**

  * (3) Fixed:  Station Agent code reworked to avoid waiting forever bug
  * (3) Fixed:  Dockware Manager was allowing capacities to be set that were higher than the dock could store
  * (3) Fixed:  Carrier Command would only run if a carrier had docked ships, which was dumb
  * (2) Fixed:  If a ship was docked at a stock exchange, it would not count towards PPP
  * (2) Fixed:  Some UT code wasn't calculating profit properly
  * (2) Fixed:  UT drone orders were fucking up trade report
  * (1) Fixed:  Station import/export display is finally shown in percentile
  * (-) Changed:  Added a few things to the market menus
  * (-) Changed:  Ship destroyed notification sound
  * (-) Changed:  Player docks hold more
  * (-) Changed:  Mass Driver added to most M5s, more M4s, some M3s
  * (-) Changed:  Vestibule of Creation sector name to Prophecy Fulfilled, as Betty was drunk.
  * (-) Changed:  Silicone Wafer volume from 18 to 12
  * (-) Changed:  The Toukon top prongs you see through the cockpit looked a little fucking stupid, so I changed them
  * (-) Changed:  Scan asteroids command no longer safes before scanning first sector
  * (-) Changed:  Asteroids, debris, no longer re-spawn
  * (-) Upgraded:  Trade Report added to context menu (advanced), hotkey added
  * (-) Upgraded:  Courier can now save, apply queues
  * (-) Upgraded:  Mobile mining implemented

---

# Version 1.3.9LU #
### October 9, 2014 ###
  * **Code base: [Zebra](http://en.wikipedia.org/wiki/Zebra)**

  * (4) Fixed:       OCV freighters were thinking they were 'stocked enough' too early
  * (-) Changed:     Increased accuracy of laser tower beam

---

# Version 1.3.8LU #
### October 8, 2014 ###
  * **Code base: [Zebra](http://en.wikipedia.org/wiki/Zebra)**

  * (4) Fixed:       OCV home sector wasn't producing wares past a count of 2000 each
  * (3) Fixed:       Revelation defend event now only starts in valid races sectors
  * (2) Fixed:       MLCC bomber debug rename
  * (2) Fixed:       Dockware Manager, coloured ship names in upgrade menu difficult to tell what was selected
  * (2) Fixed:       Dockware Manager, no longer adds equipment, upgrades, or licenses on group add
  * (2) Fixed:       Dockware Manager, Removed "Ammunition" category
  * (2) Fixed:       Terran stock exchange readtext error
  * (2) Fixed:       Revelation ATF "bounty hunter" or whatever renamed to ATF Flotilla
  * (-) Changed:     Dockware Manager menu, Upgrade Ships filters ships running commands
  * (-) Changed:     Auction Cargo Stations command now only works when docked at shipyards
  * (-) Changed:     New sector pick routine for invasion jobs
  * (-) Changed:     Limited the amount of drones a fleet will launch

---

# Version 1.3.7LU #
### October 4, 2014 ###
  * **Code base: [Zebra](http://en.wikipedia.org/wiki/Zebra)**

  * (>9000) Fixed: Fucking Kuiper belt misspelled.
  * (4) Fixed:     Flail factories were producing chaff
  * (4) Fixed:     Freighter fixed using overstock function
  * (4) Fixed:     Phanon hunters were not stopping scan task after being captured/bailed
  * (4) Fixed:     OOS laser re-balance, much testing; it's very close now.
  * (3) Fixed:     Some smaller NPC ships had no weapons or shields and it sucked
  * (3) Fixed:     UTs getting stuck on taking refuge
  * (3) Fixed:     Rep requirements for lasers
  * (3) Fixed:     MLCC bombers turret issue fixed
  * (3) Fixed:     Missile boats range check before firing tweaked, removed boarding pod selection bug
  * (3) Fixed:     M8 turret change from 1.3.3 fixed
  * (3) Fixed:     Revelation was using import values when turning Revelation back on; it shouldn't
  * (2) Fixed:     Debug spam on attacking Phanon traders removed
  * (2) Fixed:     Menu claim range versus hotkey claim range (again)
  * (2) Fixed:     Direct deposit debug spam removed
  * (2) Fixed:     Removed flickering in Plutarch Tractor System menu; optimization.
  * (2) Fixed:     Script command _add default items_ no longer adds more than max
  * (2) Fixed:     Bailed pilots of larger ships had the same stats/name
  * (1) Fixed:     Omicron Channel gates updates to Gorbs
  * (1) Fixed:     Chaff missile icon fixed
  * (1) Fixed:     Betty didn't say Alpha Particle Cannon correctly
  * (1) Fixed:     Fixed Ship Compendium ship view showing missiles for main turret
  * (-) Changed:   NPC fight routine now uses drones if available
  * (-) Changed:   Tweaked missile boat missile ranges, speeds slightly
  * (-) Changed:   Player to player station selling now adds to trade report for station
  * (-) Changed:   Some minor ship stat changes (laser: G, R, cargo: M5, M4, M3)
  * (-) Changed:   With some of the OOS combat changes, slowing OCV expansion by about 20% was necessary
  * (-) Changed:   Template outfit menu now filters ships running commands (beautiful suggestion)
  * (-) Changed:   Trade Product Search and Ship Compendium now respect ware discovery status
  * (-) Changed:   Phanon, OCV, now enemies
  * (-) Changed:   Chaff no longer destroys missiles fired by the same race
  * (-) Changed:   Ships don't bounce against drones anymore
  * (-) Changed:   Fighter drone cost, stats balanced; keris now uses plasma gun
  * (-) Changed:   Jumpdrive core costs increased, ERD requirements increased
  * (-) Changed:   Betty will no longer warn you when your ships are attacked in same sector, also increased delay between warnings
  * (-) Changed:   Humbled the engine effects
  * (-) Upgraded:  New games now load last hotkey profile
  * (-) Upgraded:  Global ship naming added ability to filter by wing and homebase
  * (-) Upgraded:  Can now remove ship types from MLCC configuration
  * (-) Upgraded:  Tahlmorra's Revelation military flash reports
  * (-) Upgraded:  All ships now have varying marine capacity (none lower than before)
  * (-) Upgraded:  Added another page to Ship Compendium showing docking capability, added marine capacity
  * (-) Upgraded:  Ship Compendium shows race in red if rep too low to buy ship
  * (-) Upgraded:  Several new script commands
  * (-) Upgraded:  Phanon, OCV now their own separate race.  The OCV are **not** Xenon.
  * (-) Upgraded:  Activate Emergency Retreat Drive hotkey implemented
  * (-) Upgraded:  Trade Product Search has new "mode" option; [TPS](Feature_Trade_Product_Search.md)
  * (-) Upgraded:  From Zebra on, save games will show data and codebase version in menus _properly_
  * (-) Upgraded:  Trade Product Search now shows some average, universally known info on wares

---

# Version 1.3.6LU #
### September 18th, 2014 ###

  * **Code base: [Cougar](http://en.wikipedia.org/wiki/Cougar_(slang))**

  * (4) Fixed:  "H!"  "Fuck" "tits!"
  * (2) Fixed:  Brain fart in station agent
  * (2) Fixed:  MLCC escorts weren't moving on to the next task when their leader left the sector in some conditions
  * (2) Fixed:  Non homebased couriers now do not have number assignments
  * (2) Fixed:  Sectors Zyarth's Dominion, Zyarth's Stand, Unknown Sector Nu, updated descriptions.
  * (2) Fixed:  Earth now a viable target for Deploy Satellite
  * (1) Fixed:  MLCC assist menu pops up again after requesting successful assist
  * (1) Fixed:  Trade product search jump now works, renamed 'dock at' just in case your autojump isn't set
  * (1) Fixed:  Betty shuts up after you start jumping on script initiated player jumps (countdown)

---

# Version 1.3.5LU #
### September 17th, 2014 ###

  * **Code base: [Ape](http://en.wikipedia.org/wiki/Ape)**

  * (5) Fixed:  Vanilla bug where if a ship was firing a missile through a turret at the same time it left a gate, game would crash.
  * (5) Fixed:  MLCC fighter wings could cause a freeze if the carrier was jumped out of sector
  * (4) Fixed:  UTs issue with black listing wares (thanks, Raaaak)
  * (4) Fixed:  TL's marine combat training had debug values still in there, enabling the class to finish in 10ish seconds.
  * (4) Fixed:  MLCC ships no longer target bailed ships / astronauts
  * (3) Fixed:  Selling missiles/shields to equipment docks was not being recorded in the trade reports properly.
  * (3) Fixed:  Scan Asteroids wasn't setting the asteroids to known
  * (3) Fixed:  One more check for Phanon traders and enemies
  * (3) Fixed:  STs were not respecting jump range (thanks, Raaaak)
  * (3) Fixed:  Docking ship could become stuck if timed right and carrier had carrier command software
  * (3) Fixed:  Carrier command software could allow more than able to dock with external docking ports.
  * (3) Fixed:  STs had a few issues in the local search code
  * (3) Fixed:  Missile chaff: mosquito missile ROF reduced, increased flash/destruction speed, eliminated spam exploit
  * (3) Fixed:  Mistral SF cockpit fixed
  * (3) Fixed:  SCH wasn't handling automatic installation of minerals from asteroids correctly
  * (3) Fixed:  ATF volunteers weren't jumping on an insurgency event
  * (3) Fixed:  OCV was searching for all race M4s in sector to base off build list, which included all freighters, resulting in more ships than necessary
  * (2) Fixed:  Stations were missing explosion effects
  * (2) Fixed:  Remote drop factory now filters out complex construction kits
  * (2) Fixed:  Remote Control System range didn't match menu claim range (formula issue)
  * (2) Fixed:  Removed template array debug spam
  * (2) Fixed:  Tugs return home if their target flagged ships were destroyed
  * (2) Fixed:  MLCC now shows "MLCC: Responding" or "MLCC: AWaiting go code", as opposed to "None" when requesting assistance
  * (1) Fixed:  Debug spam, missile ROE
  * (1) Fixed:  Pirate anarchy port replaced with pirate base
  * (1) Fixed:  SCH's "Extraneous Station Info" was showing [40](40.md) yields for stations that don't use minerals
  * (-) Changed:  Shipyard trade menu: docks show description in monitor window as opposed to a blank
  * (-) Changed:  Jumpdrive cores now registered from game start
  * (-) Changed:  UTs now refuel if jump energy is less than 8 jumps before going for a buy run
  * (-) Changed:  Script command get station best (sell/buy) price updated to include start sector; script kiddies ensure you update your scripts if you used this
  * (-) Changed:  Removed "DINK" sounds from FLC and agent level up
  * (-) Changed:  MLCC autonaming now includes homebase name; keep your MLCC dock names short
  * (-) Changed:  Mosquito missiles no longer exist; replaced with Chaff
  * (-) Changed:  Templates no longer locked to maximum of 40 jumps of energy cells
  * (-) Changed:  OCV stations start with full shields
  * (-) Changed:  Removed all object description voice overs; they didn't match all the changes anyway
  * (-) Changed:  Some missiles stats, big change on all missile prices and their respective factories
  * (-) Changed:  TLs will no longer allow you to drop an HQ if you already have one built
  * (-) Changed:  Added a 5Km distance bufffer for jumping within same sector (autojump min jump 0) to a target (with jump if distance is less than)
  * (-) Changed:  Made a new gate model as bounce was liking them
  * (-) Upgraded:  Optimized get station best price, security checks, agent behaviour
  * (-) Upgraded:  New script command: is named script on stack of task=
  * (-) Upgraded:  New script command: is sector security threat in owned scanner range: sector=, ship not a threat up to gun count=
  * (-) Upgraded:  New script command: needed jump drive energy for jumps
  * (-) Upgraded:  New script command: max jump range based on cargo energy
  * (-) Upgraded:  Reaper go home hotkey now reports and unloads as though it finished (will finish getting current ware first)
  * (-) Upgraded:  Missile chaff: Mosquito missiles, when fired, will target the nearest incoming missile, regardless of current target
  * (-) Upgraded:  New message displays for EI, various user errors, quickshuttle feedback
  * (-) Upgraded:  Changed LOD of all turrets, which made me have to realign all components (this was WAY more work than I wanted it to be)
  * (-) Upgraded:  Universe explorers and asteroid scanners will now cooperate (in a fashion), and lock sectors/asteroids
  * (-) Upgraded:  Neutral ships (bailed ships), now show up in a separate section in the sector map
  * (-) Upgraded:  Changed positioning of some trade menus so high cost items don't overlap with stock display
  * (-) Upgraded:  Ware videos removed, replaced with description of ware (many rewritten to fit in info window)
  * (-) Upgraded:  6 new sectors, Terran sectors moved, no more odd jumps (e.g. vanilla heretics end to asteroid belt)
  * (-) Upgraded:  Rewrote docking information for ships and stations to make it clearer; only 5.5 hours!
  * (-) Upgraded:  included Courier command
  * (-) Upgraded:  Fixed a performance issue with Bounce
  * (-) Upgraded:  Larxyz's LU specific HQ model implemented, now with a M6/TS docking bay
  * (-) Upgraded:  Terran have 3 new missiles, respective factories
  * (-) Upgraded:  AI ships now chaff if their fightskill is high enough
  * (-) Upgraded:  Vanilla bug: Script commands running jump on player ship respect SETA
  * (-) Upgraded:  MLCC Retreat missions now:  Escort Me: Protect, Escort Me: Attack Same, Escort Me: Attack Nearest
  * (-) Upgraded:  Larxyz's LU specific Xenon Dock model implemented
  * (-) Upgraded:  Betty now speaks all wares, including new LU wares; some ware names changed
  * (-) Upgraded:  Three tiers of CCDS (Chaff Countermeasure Defence Systems) implemented


---

# Version 1.3.4LU #
### Holy Month of Joubarbe 20, 2014 ###

  * **Code base: http://en.wikipedia.org/wiki/Sloth Sloth]**

  * _**This patch does not require an import/export**_<br><br>
<ul><li>(-) Changed: Scan asteroids autonamed<br>
</li><li>(-) Changed: Phanon traders now check for enemies like UTs do<br>
<hr />
<h1>Version 1.3.3LU</h1>
<h3>Holy Month of Joubarbe 19, 2014</h3></li></ul>

<ul><li><b>Code base: <a href='http://en.wikipedia.org/wiki/Sloth'>http://en.wikipedia.org/wiki/Sloth</a> Sloth]</b></li></ul>

<ul><li>(4) Fixed: Added safeguards to prevent a game crash if a ship docks while another ship is still launching a swam missile at it.<br>
</li><li>(4) Fixed: Shady jobs were not spawning properly<br>
</li><li>(3) Fixed: Debug spam when moving credits from station to player account via hotkey<br>
</li><li>(3) Fixed: Fighter pilot says bailing lines and stops for 10 sec, then restarts without bailing<br>
</li><li>(3) Fixed: Dockware Manager Upgrade Ship wasn't allowing install of wares after a non-compatible transport class ware<br>
</li><li>(3) Fixed: Sometimes ships jump in with zero laser energy.  The change sector recharge now only works on playership<br>
</li><li>(3) Fixed: Xenon invasion jobs were only choosing Argon sectors.  Poor fuckers.<br>
</li><li>(3) Fixed: M8 missile turrets split into two, one for offense, one for defense.<br>
</li><li>(3) Fixed: Shop for SCH bypassed station purchase rep requirements<br>
</li><li>(3) Fixed: Argon Equipment Dock capital dock lanes lowered to avoid undock collision<br>
</li><li>(3) Fixed: Station Agent was trying to buy energy cells for it's Saturn Complex Hub<br>
</li><li>(2) Fixed: Safe Undocking was attempting to run on ships that are OOS.<br>
</li><li>(2) Fixed: Penatron Advanced price fixed<br>
</li><li>(2) Fixed: Bailed ships no longer remove cargobay extension<br>
</li><li>(1) Fixed: Text changes for TS+ ships, typo with PBG<br>
</li><li>(-) Changed: Bail logging disabled<br>
</li><li>(-) Changed: Bailed ships no longer keep any ware worth over 2 million (too fragile?)<br>
</li><li>(-) Changed: Station Agent behaviour completely changed (See: <a href='Feature_Station_Agent.md'>Station Agent</a>)<br>
</li><li>(-) Changed: As you can dock at enemy pirate docks, added foe check to stations for trade routines<br>
</li><li>(-) Changed: Stations can no longer be built within a 5KM radius of a point 5KM in front of a gate<br>
</li><li>(-) Changed: McCallum and Starliner docks now renamed to equipment docks; you will have to rename already placed.<br>
</li><li>(-) Changed: Damage has greater impact on sale price<br>
</li><li>(-) Changed: Races don't hate each other as much (Terran/ATF)<br>
</li><li>(-) Changed: ATF join the fight against the OCV when the OCV reach a certain distance from home<br>
</li><li>(-) Changed: Delay on mosquito chaff effect to prevent fired missiles from being destroyed<br>
</li><li>(-) Changed: Sell Spare Equipment command now ignores currently installed missile<br>
</li><li>(-) Upgraded: Added support for Race Local variables<br>
</li><li>(-) Upgraded: Added race masking to the script engine<br>
</li><li>(-) Upgraded: Implemented Race 3-13 (+10 new races for scripts)(Reserved for future LU usage!)<br>
</li><li>(-) Upgraded: Added ability to clear a trade report<br>
</li><li>(-) Upgraded: Autonaming now handles up to 1000 ships<br>
</li><li>(-) Upgraded: Implemented Direct Deposit command (automatic station credit transfer)<br>
</li><li>(-) Upgraded: You can now set your home point through the player console<br>
<hr />
<h1>Version 1.3.2.2 Hotfix</h1>
<h3>Holy Month of Joubarbe 10, 2014</h3>
</li><li><i><b>This patch is a hotfix, and must be applied on top of 1.3.2 - Contains changes in the 1.3.2.1 Hotfix</b></i>
</li><li><i><b>This hotfix does not require Export/Import</b></i>
</li><li>(5) Fixed: Lockup being cause by a corrupted M2MD script due to a compiler error and incorrect usage of a command.<br>
<hr />
<h1>Version 1.3.2.1 Hotfix</h1>
<h3>Holy Month of Joubarbe 7, 2014</h3>
</li><li><i><b>This patch is a hotfix, and must be applied on top of 1.3.2 - it does not contain changes from any previous patch.</b></i>
</li><li><i><b>This hotfix does not require Export/Import</b></i>
</li><li>(5) Fixed: Lockup being caused by in sector combat related to captial ships & M2MD scripts.<br>
<hr />
<h1>Version 1.3.2</h1>
<h3>Holy Month of Joubarbe 6, 2014</h3>
</li><li><i><b>This patch requires an import/export; exports from V1.2.5 and up are compatible.  See: <a href='Feature_Export_Import.md'>Export/Import</a></b></i><br><br>
</li><li>(5) Fixed: SIGNAL_TARGETED was accidentally starting SIGNAL_ATTACKED's command script causing the player to loose control of their ship<br>
</li><li>(4) Fixed: EI was not syncing job times (spawning everything it could on the start when EI set game time)<br>
</li><li>(4) Fixed: OWPs no longer bail<br>
</li><li>(-) Changed: Bails tuned<br>
<hr />
<h1>Version 1.3.1</h1>
<h3>Holy Month of Joubarbe 3, 2014</h3>
</li><li><i><b>This patch requires an import/export; exports from V1.2.5 and up are compatible.  See: <a href='Feature_Export_Import.md'>Export/Import</a></b></i><br><br>
</li><li>(4) Fixed: Fighters breaking off attacks too early<br>
<hr />
<h1>Version 1.3.0</h1>
<h3>Holy Month of Joubarbe 3, 2014</h3>
</li><li><i><b>This patch requires an import/export.  See: <a href='Feature_Export_Import.md'>Export/Import</a></b></i><br>
</li><li><i><b>This patch requires a reinstall of the base mod</b></i><br><br>
</li><li>(2) Changed: Context menu remote system control software wasn't set to 4Km<br>
</li><li>(-) Changed: Joubarbe's moon fixed (Thyn's Excavation)<br>
</li><li>(-) Changed: Xenon Sector 472 has it's shattered planet now<br>
</li><li>(-) Changed: Removed salvager name highlighting<br>
</li><li>(-) Changed: Hull requirements before bailing is even considered have been tweaked (lower value)<br>
</li><li>(-) Changed: Bailing now only has once chance per 5 minutes<br>
</li><li>(-) Changed: Crate drops are now slightly less than half as frequent<br>
</li><li>(-) Upgraded: Signal_Targeted now implemented (Jack08's code)<br>
</li><li>(-) Upgraded: Special routine for capital ships with main guns to minimize ramming</li></ul>

<hr />
<h1>Version 1.2.5</h1>
<h3>Joubarbe 2, 2014</h3>
<ul><li><i><b>This patch requires an import/export.  See: <a href='Feature_Export_Import.md'>Export/Import</a></b></i><br>
</li><li><i><b>Patch contains all previous changes from 1.2.1 and up</b></i><br><br>
</li><li>(4) Fixed: emergency jump had issues when OOS<br>
</li><li>(4) Fixed: emergency jump with an ERD wasn't jumping when it lacked cores<br>
</li><li>(3) Fixed: Collect wares command now works in same sector if ship is docked<br>
</li><li>(1) Fixed: Terran's lasertower icon is now a laser tower icon as opposed to an M5 icon<br>
</li><li>(1) Fixed: A few more safeguards implemented to keep people from fucking up ships names and export compatibility<br>
</li><li>(-) Changed: Reduced range of Remote System Control to 4Km<br>
</li><li>(-) Changed: Missile to missile defence now only works with M8s<br>
</li><li>(-) Changed: M8s will no longer dock while following (due to M2MD)<br>
</li><li>(-) Changed: Phanon shop list updated<br>
</li><li>(-) Upgraded: Modders have a way of registering stuff in the EI (<a href='Modders_Resource_RegisterEI.md'>Modders Resource: Register to EI</a>)<br>
</li><li>(-) Upgraded: Universal bailing implemented (See: <a href='Feature_Universal_Bailing.md'>Universal Bailing</a>)<br>
</li><li>(-) Upgraded: Implemented salvager jobs to clean up<br>
</li><li>(-) Upgraded: All job patrol scripts rewritten; patrols will no longer smile/wave/moon/flash tits as they fly by enemies<br>
</li><li>(-) Upgraded: Phanon corp subsidiaries can now be fired if their performance is low<br>
<hr />
<h1>Version 1.2.4</h1>
<h3>July 28, 2014</h3>
</li><li><i><b>This patch requires an import/export.  See: <a href='Feature_Export_Import.md'>Export/Import</a></b></i><br>
</li><li><i><b>Patch contains all previous changes from 1.2.1 and up</b></i><br><br>
</li><li>(4) Fixed: MLCC fighters stopping when no enemy within carrier's set range<br>
</li><li>(2) Fixed: Reaper reporting incorrect number of wares collected<br>
</li><li>(2) Fixed: Encyclopedia showing readtext0-0 when item with no info was selected<br>
</li><li>(-) Changed: Fuel Quickshuttle (and all supply commands) now return home to load if wares available<br>
</li><li>(-) Upgraded: Implemented <a href='Feature_Missile_Boat_Missile_Defence.md'>Missile Boat Missile Defence</a>
</li><li>(-) Upgraded: Added Terran ice mines for sale<br>
</li><li>(-) Upgraded: New weapon lighting effects<br>
<hr />
<h1>Version 1.2.3</h1>
<h3>July 14, 2014</h3>
</li><li><i><b>This patch does not require an import/export</b></i>
</li><li><i><b>Patch contains all previous changes from 1.2.1 and up</b></i><br><br>
</li><li>(3) Fixed: FLC in rainmeter (skin updated to 1.3 on download page)<br>
<hr />
<h1>Version 1.2.2</h1>
<h3>July 13, 2014</h3>
</li><li><i><b>This patch does not require an import/export</b></i>
</li><li><i><b>Patch contains all previous changes from 1.2.1 and up</b></i>
</li><li><i><b>This patch requires you to first install the GUI Installer from the <a href='02_Download_Instructions.md'>Download Page</a></b></i><br><br>
</li><li>(4) Fixed: imported Phanon Corp resets when it's not supposed to<br>
</li><li>(3) Fixed: MLCC ships no longer load energy in place of missiles when restocking<br>
</li><li>(3) Fixed: ships were loading entire amount of missiles or tech wares (jump cores) when docking<br>
<hr />
<h1>Version 1.2.1</h1>
<h3>July 12, 2014</h3>
</li><li><i><b>This patch does not require an import/export</b></i><br><br>
</li><li>(3) Fixed: rainmeter script<br>
</li><li>(3) Fixed: UT purchasing amount now respects fuel resupply like agents do<br>
</li><li>(2) Fixed: Qlaser set rapid fire exploit<br>
</li><li>(2) Fixed: command "None" again; oh, X-Studio<br>
</li><li>(1) Fixed: command help descriptions<br>
</li><li>(-) Upgraded: more Curlsworth loadscreens<br>
<hr />
<h1>Version 1.2.0</h1>
<h3>July 11, 2014</h3>
</li><li><i>Patch contains all previous changes from 1.1.3 and up</i><br>
</li><li><i><b>This patch requires an import/export to fix known issues.  See: <a href='Feature_Export_Import.md'>Export/Import</a></b></i><br><br>
</li><li>(5) Fixed: <b>finally</b> tracked down this Phanon Corp negative laser bug (causes a crash when the ship is destroyed, rare)<br>
</li><li>(3) Fixed: Carriers (including MLCC carriers) were loading more than they should when docking<br>
</li><li>(3) Fixed: capital ships with main guns now use default attack routine<br>
</li><li>(3) Fixed: dreadnoughts were supposed to have boarding defences built in<br>
</li><li>(3) Fixed: UT: prefuel errors weren't reporting properly, possible causing UTs to fly without jumping<br>
</li><li>(3) Fixed: retreating MLCC ships would sometimes retreat one at a time<br>
</li><li>(3) Fixed: after 4 years, fixed Phanon Corporation morale issue for ships<br>
</li><li>(3) Fixed: UTs should no longer jump to enemy sectors when attacked<br>
</li><li>(2) Fixed: Trade report shows incorrect price for items purchased when upgrading multiple ships at shipyard simultaneously<br>
</li><li>(2) Fixed: Missile safety issue with ships destroyed before missile safety turns off<br>
</li><li>(2) Fixed: vanilla exploit: collecting a shield ware from space instantly resets a ship's shields<br>
</li><li>(2) Fixed: PX shields wrong<br>
</li><li>(2) Fixed: collecting credits with the collect ware command caused credits to be installed into the ship<br>
</li><li>(2) Fixed: PX left turret config was set to front<br>
</li><li>(2) Fixed: Rainmeter skin now shows ranks (you'll have to download the new LU for Rainmeter update)<br>
</li><li>(2) Fixed: implemented Laserzwölf und 1's changes for station agent picking manage wares<br>
</li><li>(2) Fixed: station transfer credit set low water mark menu wasnt remembering, minimum was 1000<br>
</li><li>(1) Fixed: typos on EBC, HEPT descriptions<br>
</li><li>(1) Fixed: did a thing in tug command, and added a version checker<br>
</li><li>(-) Changed: M6, TM, TS, TP do not wait for gate jumps anymore (wasn't TC this way??)<br>
</li><li>(-) Changed: added marines to commonwealth ships<br>
</li><li>(-) Changed: jumping no longer restores laser energy<br>
</li><li>(-) Changed: sector greek letters capitalized<br>
</li><li>(-) Changed: player stat "Ships captured" changed to "Ships bailed"<br>
</li><li>(-) Changed: no stations within 12 KM of each other or within 8 KM of gate lanes, sector size changes and station rearrangements<br>
</li><li>(-) Upgraded: MLCC task descriptions fixed<br>
</li><li>(-) Upgraded: MLCC bomber task reworked, now a turret setting and monitor routine<br>
</li><li>(-) Upgraded: MLCC new task added: escort<br>
</li><li>(-) Upgraded: Added modernized version of set global homebase /w search string<br>
</li><li>(-) Upgraded: Added TrixX's LU weapon/missile icons<br>
</li><li>(-) Upgraded: weapon effects; all weapons now have light for impact and launch, cleaned up a few, organized effects.txt<br>
</li><li>(-) Upgraded: added script command <i>add marines</i>
</li><li>(-) Upgraded: added script command <i>add default equipment</i>
</li><li>(-) Upgraded: added script command <i>bail ship</i>
</li><li>(-) Upgraded: added script command <i>eject ware</i>
</li><li>(-) Upgraded: Phanon Corporation loadouts change per generation<br>
</li><li>(-) Upgraded: Phanon Corporation traders now eject wares, jump away<br>
</li><li>(-) Upgraded: new Curlsworth load screens</li></ul>




<hr />
<h1>Version 1.1.9</h1>
<h3>July 7, 2014</h3>
<ul><li><i>Patch contains all previous changes from 1.1.3 and up</i><br>
</li><li><i><b>This patch does not require an import/export</b></i><br><br>
</li><li>(5) Fixed: forgot a dot at the end of the Damyath Light description<br>
</li><li>(5) Fixed: implemented Jack08's fix for some money issues, rendering no credits withdrawn<br>
</li><li>(5) Fixed: implemented Jack08's search lockup fix<br>
</li><li>(3) Fixed: Valhalla can't turn (among other dreadnoughts)<br>
</li><li>(3) Fixed: Hammerhead missile factory not available in SCH menu was caused by it not actually being sold (galaxy map fix)<br>
<ul><li>(3) Fixed: Pirate Buster cannot fire<br>
</li></ul></li><li>(3) Fixed: Phanon Corp sets up in Kingdom end if their HQ was destroyed when performing EI<br>
</li><li>(3) Fixed: shouldn't be more than one valhalla in the universe<br>
</li><li>(2) Fixed: escaping the remote drop factory command brought up the galaxy menu<br>
</li><li>(2) Fixed: Dock agents don't sell the same ware at the same time anymore<br>
</li><li>(1) Fixed: removed a debug message from collect astronaut<br>
</li><li>(-) Changed: Quickshuttle selection menu uses new selection display<br>
</li><li>(-) Changed: DWM template outfit allows all stations to be set to homebase<br>
</li><li>(-) Upgraded: Dockware Manager sources and thresholds now sorted</li></ul>

<hr />
<h1>Version 1.1.8</h1>
<h3>June 27, 2014</h3>
<ul><li><i>Patch contains all previous changes from 1.1.3 and up</i><br>
</li><li><i><b>This patch does not require an import/export</b></i><br><br>
</li><li>(4) Fixed: SCH not adding secondary resources (disengage, reengage after patch)<br>
</li><li>(4) Fixed: FINALLY fixed the damn nav sat export bug; typo.<br>
</li><li>(3) Fixed: Rainmeter skin FLC display, added to download page<br>
</li><li>(2) Fixed: pirate penatron advanced augmented<br>
</li><li>(1) Fixed: SCH debug spam.<br>
<hr />
<h1>Version 1.1.7</h1>
<h3>June 26, 2014</h3>
</li><li><i>Patch contains all previous changes from 1.1.3 and up</i><br>
</li><li><i><b>This patch requires an import/export to fix known issues.  See: <a href='Feature_Export_Import.md'>Export/Import</a></b></i><br><br>
</li><li>(5) Fixed: a bug in Station Agent that would cause a hang<br>
</li><li>(4) Fixed: MLCC threat assesment for sortie fixed<br>
</li><li>(3) Fixed: build station mission was requesting an SCH build<br>
</li><li>(3) Fixed: EI bug - Fenrirs / shields: import now adds tunings first (fenrirs didn't have cargo space)<br>
</li><li>(3) Fixed: Dockware manager was allowing more than what should have been allowed to be purchased<br>
</li><li>(3) Fixed: Tug docking rewritten; tested, and no stuck ships<br>
</li><li>(3) Fixed: player traders only selling 250 of ware when more viable trade ops exist<br>
</li><li>(3) Fixed: Dockware Manager - Upgrade Ships was allowing transport class restricted wares to be bought for ships<br>
</li><li>(3) Fixed: by Jack08, uncool race ship blueprints being sold<br>
</li><li>(3) Fixed: some stock exchange sotck set a max 0 trades, as a result, max trading per transaction a time is limited to 500,000,000 credits<br>
</li><li>(3) Fixed: astronauts were disappearing when using collect astronaut command<br>
</li><li>(3) Fixed: HQ now docks produced ships properly; if there's a docking port available it will create the ship properly<br>
</li><li>(2) Fixed: defend station mission no longer sends odd reward message<br>
</li><li>(2) Fixed: move to position now works properly<br>
</li><li>(2) Fixed: some laser energy requirements fixed<br>
</li><li>(2) Fixed: Xenon invasion mission no longer sends odd reward message<br>
</li><li>(2) Fixed: type fixed in ship info menu<br>
</li><li>(2) Fixed: debug spam in ship outfit template<br>
</li><li>(2) Fixed: player ship couldn't be teleported with the carrier command software<br>
</li><li>(2) Fixed: collect ware instantly teleporting ware despite range<br>
</li><li>(2) Fixed: Collect wares would get stuck on transport class error<br>
</li><li>(1) Fixed: UTs now use the LU Refuel.Pre routine, eliminating breaking the sector rules for refuelling UTs<br>
</li><li>(1) Fixed: Saturn SCH Shop weirdness with no SCH selected<br>
</li><li>(1) Fixed: mouse now works on custom menu value sliders<br>
</li><li>(1) Fixed: Pirate bayamon cargo fixed<br>
</li><li>(1) Fixed: ship claiming set to vanilla default routine when using remote system command software<br>
</li><li>(1) Fixed: IPG descriptions<br>
</li><li>(1) Fixed: docks/shipyards no longer spawn in player, xenon, khaak or khaak owned sectors<br>
</li><li>(-) Changed: Terran used ships now offered<br>
</li><li>(-) Changed: a label in Tug, hope it helps from getting ships stuck<br>
</li><li>(-) Changed: docking no longer sets shields to 100% (this was far more work than you may think)<br>
</li><li>(-) Changed: orbital weapon platforms weapon load-outs adjusted.<br>
</li><li>(-) Changed: Gamma Ray Cannon notoriety required<br>
</li><li>(-) Changed: flagship entourage augmented<br>
</li><li>(-) Changed: some M2 transport classes<br>
</li><li>(-) Changed: Pirate plunderers range expanded<br>
</li><li>(-) Changed: renamed "Allow station transfer" to "Include in credit transfer"<br>
</li><li>(-) Changed: removed a planet to make Argon Prime socks fit in window (stock amounts are based on planet count)<br>
</li><li>(-) Changed: renamed "Drop Factory" to "Remote Drop Factory" and disabled use IS<br>
</li><li>(-) Changed: rewrote Drop Factory description<br>
</li><li>(-) Changed: removed flight times and set global homebase<br>
</li><li>(-) Changed: removed marine search command<br>
</li><li>(-) Changed: removed transport ships command<br>
</li><li>(-) Changed: ship accelerations tweaked<br>
</li><li>(-) Changed: Bounce removed for Terran stations and astronaunts<br>
</li><li>(-) Changed: Bounce added for capital ships<br>
</li><li>(-) Changed: HUD missile readout position changed by a few pixels<br>
</li><li>(-) Changed: Pirate and Yaki trading same as Teladi now in terms of notoriety req. to buy ships, certain wares, etc<br>
</li><li>(-) Changed: trade product search now ignores player stations and empty buy stations<br>
</li><li>(-) Changed: Remote Drop Factory no longer supports dropping mines<br>
</li><li>(-) Upgraded: missile safety implemented (with distance check, not time)<br>
</li><li>(-) Upgraded: new script command: set menu option: , icon=<br>
</li><li>(-) Upgraded: new script command: = format number: number= , billions= , format wrapper=<br>
</li><li>(-) Upgraded: new script command: = sum billion arrays: first= , second=<br>
</li><li>(-) Upgraded: new script command: = add to billion array: array= , number=<br>
</li><li>(-) Upgraded: new script command: = multiply billion array: array= , number=<br>
</li><li>(-) Upgraded: every ship and station now has a trade report<br>
</li><li>(-) Upgraded: trade report now handles quadrillions<br>
</li><li>(-) Upgraded: Move Logistics command modernized and added to SCH wiki<br>
</li><li>(-) Upgraded: new script command: get shipyards sells ware: ware=, jumps=, flags=, exclude=<br>
</li><li>(-) Upgraded: Supply Ware Command easier menu<br>
</li><li>(-) Upgraded: Trade Product Search easier menu, moved to dynamic<br>
</li><li>(-) Upgraded: Tractor Asteroid menu modernized<br>
</li><li>(-) Upgraded: modernized Global ship renaming tool in player console; it's pretty slick now.<br>
</li><li>(-) Upgraded: Ship Info menu renamed Ship Compendium, loads substantially faster, now must know shipyard to see ship<br>
</li><li>(-) Upgraded: SCH & SCH calculator now LU dynamic menu; also supports quadrillion credit displays<br>
</li><li>(-) Upgraded: SCH EI now fully supported.  Partially build SCH, engaged SCH, etc. all EI appropriately<br>
</li><li>(-) Upgraded: ship and station info menus now show all dock port capabilities depending on class<br>
</li><li>(-) Upgraded: buy/sell signal added to shipyard<br>
</li><li>(-) Upgraded: non-script safe undocking implemented<br>
</li><li>(-) Upgraded: FLC display added to player menu<br>
</li><li>(-) Upgraded: flag for tug is now a toggle; can unflag a ship<br>
</li><li>(-) Upgraded: station friendly fire implemented<br>
</li><li>(-) Upgraded: collect astronauts can now use transporter device<br>
</li><li>(-) Upgraded: relation/trade rank change subtitle now shows race or rank type<br>
</li><li>(-) Upgraded: EI from 1.1.7 on no longer requires moving/renaming the export file.</li></ul>



<hr />
<h1>Version 1.1.6</h1>
<h3>June 6, 2014</h3>
<ul><li><i>Patch contains all previous changes from 1.1.3 and up</i><br><br>
</li><li>(3) Fixed: accidentally overwrote Panther name with description<br>
</li><li>(-) Changed: TM weapon energy, recharge rate augmented<br>
</li><li>(-) Changed: Dumbfire missiles removed from capital ships<br>
<hr />
<h1>Version 1.1.5</h1>
<h3>June 5, 2014</h3>
</li><li><i>Patch contains all previous changes from 1.1.3 and up</i><br><br>
</li><li>(4) Fixed: "FLC, Motherfucker!" debug text removed.<br>
<hr />
<h1>Version 1.1.4</h1>
<h3>June 5, 2014</h3>
</li><li><i>Patch contains all previous changes from 1.1.3 and up</i><br><br>
</li><li>(4) Fixed: Export would be bugged if you owned a navigational satellite<br>
</li><li>(2) Fixed: Dockware manager was adding ammunition when adding HQ ware group<br>
</li><li>(1) Fixed: Dock Agent & Station Agent over 100% XP bug<br>
</li><li>(-) Changed: Reduced the time the tug would wait to restart ships getting stuck docking.<br>
</li><li>(-) Changed: stock exchange available stocks now shows.. what's available.. (total - owned)<br>
</li><li>(-) Changed: stock exchange menu title now cleaner<br>
</li><li>(-) Changed: Move Freight command renamed to Freighter<br>
</li><li>(-) Changed: Get Fuel command description<br>
</li><li>(-) Changed: Sector trader ranges tweaked very slightly<br>
</li><li>(-) Changed: Panther description<br>
</li><li>(-) Changed: removed Dock Agent & Station Agent log entries for level up<br>
</li><li>(-) Changed: Sector Trader ship names now automated and standardized<br>
</li><li>(-) Changed: mosquito missile agility increased<br>
</li><li>(-) Upgraded: overhauled template manager menu, more accessible display<br>
</li><li>(-) Upgraded: Dock Agent & Station Agent more informative task tags, no more station not found messages<br>
</li><li>(-) Upgraded: Missile Only turret command run on missiles boats now runs a special mosquito missile defence<br>
<hr />
<h1>Version 1.1.3</h1>
<h3>June, 3, 2014</h3>
</li><li><i>Patch contains all previous changes from 1.0.1 and up</i>
</li><li>(4) Fixed: Dockware Manager could sometimes incorrectly removing deprecated wares; showed Impulse Ray Emitters in trade menu<br>
</li><li>(3) Fixed: Trading would sometimes return no station found for equipment wares<br>
</li><li>(3) Fixed: Station Agent wasn't pausing on manage when station set to standby<br>
</li><li>(3) Fixed: 4 Terran weapon forges were not sold in Uranus as they should have been; map fix only on new start<br>
</li><li>(3) Fixed: Dockware Manager would not add wares with <i>set group</i> in some circumstances<br>
</li><li>(3) Fixed: Tug bug was sending tug to pickup ship at location even if it was already docked<br>
</li><li>(3) Fixed: Barracuda Advanced couldn't fire weapons<br>
</li><li>(3) Fixed: Logich was using commonwealth missiles<br>
</li><li>(2) Fixed: Pirate Penatron description text added<br>
</li><li>(2) Fixed: Export/Import no longer starts UT when it wasn't running the command<br>
</li><li>(2) Fixed: Export/Import starts sector traders properly<br>
</li><li>(2) Fixed: Dockware Manager would show null% storage when capacity was set to 0<br>
</li><li>(1) Fixed: Quickshuttle typo in hotkeys; won't change until an import/export, but very minor<br>
</li><li>(1) Fixed: Constaculating the influxuation of depesthetic congluancies no longer runs until an import is finished<br>
</li><li>(1) Fixed: typo in SCH calculator<br>
</li><li>(1) Fixed: spelling errors in several messages from Phanon and Revelation.<br>
</li><li>(1) Fixed: spelling errors in Omicron Channel sector descriptions; you should read them<br>
</li><li>(1) Fixed: a few lasers and ships still had <i>Betty</i> descriptions; all are now stripped<br>
</li><li>(1) Fixed: Nova Prototype description was missing<br>
</li><li>(-) Changed: station allow NPC trading flag name to "Station is open for trading" to better reflect its purpose in LU<br>
</li><li>(-) Changed: Station Agent class changed to freighter<br>
</li><li>(-) Changed: Fuel Quickshuttle now requires supply command software<br>
</li><li>(-) Changed: Carrier Command Software can now only be used by huge ships<br>
</li><li>(-) Changed: Explorer Command Software added to two more docks; map fix only on new start<br>
</li><li>(-) Changed: Completely removed repair laser from all turrets<br>
</li><li>(-) Upgraded: Quickshuttle Fuel rewritten; wiki updated<br>
</li><li>(-) Upgraded: Supply Command Software now able to provide equipment wares<br>
</li><li>(-) Upgraded: Export/Import speed slightly optimized<br>
</li><li>(-) Upgraded: Export/Import now saves Phanon Corporation's current sector<br>
</li><li>(-) Upgraded: Export/Import now imports mineral mine stations properly<br>
</li><li>(-) Upgraded: Export/Import now saves turret command configurations<br>
</li><li>(-) Upgraded: Export/Import now saves wings<br>
</li><li>(-) Upgraded: Rearm rewritten<br>
</li><li>(-) Upgraded: Refuel rewritten<br>
</li><li>(-) Upgraded: Stock exchange slider now maxes out at what you can afford, and also takes into account tariff costs<br>
</li><li>(-) Upgraded: Missile descriptions rewritten, <i>Betty</i> descriptions completely stripped<br>
</li><li>(-) Upgraded: Tug now has ship stripping options<br>
</li><li>(-) Upgraded: Added LU descriptions for lasers AKE, BKE, GKE, PBC, RL<br>
</li><li>(-) Upgraded: Added LU descriptions for OCV ships O, deca.fade, PX, R, G, V, T</li></ul>



<hr />
<h1>Version 1.1.2</h1>
<h3>May, 29, 2014</h3>
<ul><li><i>Patch contains all previous changes from 1.0.1 and up</i>
</li><li>(4) Fixed: Trade Run: Sell could crash when selling energy cells<br>
<hr />
<h1>Version 1.1.1</h1>
<h3>May, 29, 2014</h3>
</li><li><i>Patch contains all previous changes from 1.0.1 and up</i>
</li><li>(1) Fixed: Revelation message was displaying sector as null<br>
</li><li>(1) Fixed: Fighter was listed twice in ERD description<br>
</li><li>(-) Upgraded:  Marine Training command overhauled<br>
<hr />
<h1>Version 1.1.0</h1>
<h3>May, 28, 2014</h3>
</li><li><i><b>This patch requires an import/export to fix known issues.  See: <a href='Feature_Export_Import.md'>Export/Import</a></b></i>
</li><li><i>Patch contains all previous changes from 1.0.1 and up</i>
</li><li><i>Really</i> sorry I had to do this, but this patch is necessary to maintain future compatibility with 3rd party export/import shit.<br>
<hr />
<h1>Version 1.0.7</h1>
<h3>May, 28, 2014</h3>
</li><li><i><b>This patch requires an import/export to fix known issues.  See: <a href='Feature_Export_Import.md'>Export/Import</a></b></i>
</li><li><i>Patch contains all previous changes from 1.0.1 and up</i>
</li><li>Fixed: logbook number spam<br>
</li><li>Fixed: serious issue with UT signals; bug is very rare, but problematic<br>
</li><li>Fixed: dock agent, station agent, UT attacked scripts now stop when they've been re-purposed<br>
</li><li>Fixed: deploy satellite center config shouldn't re-place center sats anymore<br>
</li><li>Fixed: station agent may switch to <i>manage</i> after being attacked<br>
</li><li>Fixed: deploy satellite menu debug spam removed<br>
<hr />
<h1>Version 1.0.6</h1>
<h3>May, 27, 2014</h3>
</li><li><i>Patch contains all previous changes from 1.0.1 and up</i>
</li><li>Fixed: Station Agent not resetting properly when new script version detected (resets to manage, always).<br>
<hr />
<h1>Version 1.0.5</h1>
<h3>May, 27, 2014</h3>
</li><li><i>Patch contains all previous changes from 1.0.1 and up</i>
</li><li>Fixed: some spelling errors<br>
</li><li>Fixed: non-transporter device collect wares in sector only collecting 1 ware, then idling<br>
</li><li>Fixed: build station briefing<br>
</li><li>Fixed: Mandalay description<br>
</li><li>Fixed: jumping with carried ships forcing ship to fly through gates<br>
</li><li>Fixed: Carrier Command Software was allowing too many ships to dock<br>
</li><li>Fixed: "wait past station chan" debug log removed<br>
</li><li>Fixed: Reap shuttle wasn't set correctly, giving you an error tone  Reset your reap shuttle in player console<br>
</li><li>Fixed: After considering a specific bug, big TS ships back to XL cargo classes.  TLs need a place<br>
</li><li>Fixed: Argon Mammoth sold at Family Pride shipyard removed<br>
</li><li>Fixed: Vulture Prototype rear turret only mounted repair laser<br>
</li><li>Fixed: Dock Agents now play nice together.  Dock agents won't buy the same ware at the same time, and won't overstock (unless flagged to)<br>
<hr />
<h1>Version 1.0.4</h1>
<h3>May, 15, 2014</h3>
<ul><li><i>Patch contains all previous changes from 1.0.1 and up</i>
</li><li>Changed version display<br>
<hr />
<h1>Version 1.0.3</h1>
<h3>May, 12, 2014</h3>
</li><li><i>Patch contains all previous changes from 1.0.1 and up</i>
</li><li>Added docking music.<br>
<hr />
<h1>Version 1.0.2</h1>
<h3>May, 12, 2014</h3>
</li><li><i>Patch contains all previous changes from 1.0.1 and up</i>
</li><li>Fixed: Tships test issue (Aamon super ship).<br>
<hr />
<h1>Version 1.0.1</h1>
<h3>May, 12, 2014</h3>
</li><li>Fixed: read text error for lasers.<br>
<hr />
<h1>Version 1.0.0</h1>
<h3>May, 11, 2014</h3>
</li></ul></li><li>Release<br>
<hr />