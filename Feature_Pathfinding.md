# Pathfinding #

Don't you hate it when you just bought a ship in Queens Harbour, and it needs to get to Argon Prime, you send it on its way, and you have to baby sit it to ensure it doesn't fly through Xenon or Pirate sectors?

Sector pathfinding is implemented in every facet of the game now.  When using the Navigation Command Software Mk1, you can use commands to "fly safe", which enables the ship to avoid all sectors that the ship has set to foe.

Traders who don't have a jump drive (Station Agent, Dock Trader, UT, Freighter, etc.) search for close trades _based on flying safe_.  In other words, if there's a good trade on the other side of Farnham's Legend that seem lucrative and closer, and your jumpless trader chooses one a few sectors away instead, consider that that the path to the first trade was longer, considering it had to avoid Farnham's Legend, a pirate sector, to get to that destination.

Other jumpless scripts also use foe pathfinding, such as deploy satellites.

In the image below, you can see a ship's navigation menu with the Navigation Command Software Mk1 installed, illustrating the fly safe commands.

![http://www.mediafire.com/convkey/e73c/8744zp6542sj584fg.jpg](http://www.mediafire.com/convkey/e73c/8744zp6542sj584fg.jpg)