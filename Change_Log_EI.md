# Change Log #


### Legend ###
  * 1 = Very minor
  * 2 = Minor
  * 3 = Average
  * 4 = Critical
  * 5 = Seriously Fucking Critical
  * EI is an acronym for Export/Import



---

# Version 2.2.0EI #
### November 7, 2014 ###
  * (4) Fixed:  If you tried to export a version less than 1.3.5 to a newer vesion, hang could happen with revelation importing

---

# Version 2.1.9EI #
### October 31, 2014 ###
  * (5) Fixed:  Fucking efficiency on Mines was not set properly

---

# Version 2.1.8EI #
### October 26th, 2014 ###
  * (5) Fixed:  OCV ship export

---

# Version 2.1.5EI #
### October 24th, 2014 ###
  * (-) Changed:  EI recreates all asteroids/debris
  * (-) Upgraded:  Courier save queue support

---

# Version 2.1.4EI #
### October 9, 2014 ###
  * (-) Changed:  Phanon, OCV messages on EI suppressed
  * (-) Changed:  LU.EI.IgnoreThis will ignore the object during export

---

# Version 2.1.3EI #
### October 4, 2014 ###
  * (2) Fixed:  Safeguard to prevent an export within the first 5 minutes of a game.  Shit needs to be setup before you export.
  * (-) EI implemented:  Ware discovered status

---

# Version 2.1.2EI #
### September 18, 2014 ###
  * (2) Fixed:  EI wasn't putting player in correct sector after complex connections
  * (1) Fixed:  Small check for < and > characters

---

# Version 2.1.1EI #
### September 18, 2014 ###
  * (2) Fixed:  Sector/Map change support for versions older than 1.3.4

---

# Version 2.1.0EI #
### September 17, 2014 ###
  * (2) Fixed:  Salvage insurance no longer doubles
  * (2) Fixed:  Dock Agent, Freighter also get stray ware cleanup
  * (1) Fixed:  Laser towers import as already setup
  * (-) EI implemented:  Complex connections
  * (-) EI implemented:  Dock MLCC is installed
  * (-) EI implemented:  MLCC Tasks
  * (-) EI implemented:  MLCC Missile ROEs
  * (-) EI implemented:  MLCC Hangar info
  * (-) EI implemented:  Stock exchange stocks, no longer have to empty stock exchange before EI
  * (-) EI implemented:  Ships now put into environment if it was owned by player (i.e. ship or station)
  * (-) EI implemented:  Qshuttles
  * (-) EI implemented:  Autostart supported:  UT, ST, Station Agent, Dock Agent, Freighter, Attack Nearest, Attack Same, Protect, Deploy Satellites, Explore Universe, Scan Asteroids, Tug

<br>
<b>Notes on this version</b>
<ul><li>Exporting from less than LU1.3.5 to newer version:<br>
<ul><li>1) Bad news: Your ships will not autostart, you will have to reissue new commands and ensure cargo bays are empty.<br>
</li><li>1) Good news: From version LU1.3.5 on, several scripts will autostart after an EI (see patch notes)<br>
</li><li>2) Bad news: If you have <a href='http://forum.egosoft.com/viewtopic.php?t=336717'>this</a> script installed, your EI will fail.  You'll have to remove the escape codes manually using a text editor.<br>
</li><li>2) Good news: From version LU1.3.5 on, the EI properly strips this error out.<br>
</li><li>3) Bad news: MLCC will be uninstalled on all docks.<br>
</li><li>3) Good news: From version LU1.3.5 on, MLCC is properly E/I'd.