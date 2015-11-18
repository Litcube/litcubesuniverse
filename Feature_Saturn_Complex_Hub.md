# Saturn Complex Hub #

The Saturn Complex Hub is a dynamic complex within a single station

## Hey, I Remember This! ##

No you don't.  No one downloaded it.

![http://www.mediafire.com/convkey/3640/gubom344oa0kh98fg.jpg](http://www.mediafire.com/convkey/3640/gubom344oa0kh98fg.jpg)

# Backstory #

Finally, the Terrans have contributed to the Universal economic sciences. Recently discovered and patented compounds discovered in the inner rings of Saturn have led to rapid discoveries in unprecedented cargo compression. The first foray into the manifestation of this highly secretive substance has been implemented in a customized Terran complex hub. As a first sign of interstellar co-operation extended from Terrans to Commonwealth, a new shipyard has been deployed in sector Saturn 3, stocked with all 400 models of the new Saturn Complex Hub. The Saturn Complex Hub allows a company owner to install massive and scalar production complexes within a single station, reducing sector clutter, and most importantly, confining all intermediary resources within the station.

# What is a Saturn Complex Hub? #

Essentially, a Saturn Complex Hub is a single station, based on the Terran Crystal Fab model. Once deployed and configured correctly, it acts as a normal factory producing a single ware, with no resources required, as per a self-sustaining complex. I've modified the model to contain a capital dock port and 20 freighter arms. There's 400 variations, each representing a product's production capability, but otherwise identical. However, it's not a cheating factory. For those wishing for a simple and easy "remove resources" factory, look elsewhere.

Benefits:
  * Doesn't cheat.
  * Produce the same amount of wares without the FPS bog of vanilla complexes
  * No more /!\ flashing stations; no resources required.
  * Needed factories can be automatically purchased by your TL.
  * Easy to use.

The Saturn Complex Hub must be fitted with all of the stations as would a regular complex. Here's how:

# How do I set up my Saturn Complex Hub? #

_Keep in mind, there's a hotkey for a SCH Calculator that you can set. From here you can play around with all sizes of SCHs and see what the expected cost to setup your SCH will be (All without actually purchasing a SCH)_

Fly a TL to Saturn 3. Dock at the shipyard in that sector. You'll see a whole load of Saturn Complex Hubs for sale. The number after the sale item is the "production" of the module itself. As a reference, M sized factories would be the equivalent of a Saturn Complex Hub 002, and an L sized factory would be the equivalent of a Saturn Complex Hub 005. They go all the way up to 400. Once deployed from your TL's cargo hold as you would a regular factory in a sector of your choosing (preferably with a lot of scanned asteroids), select the command "Saturn Hub Console" under the command console of the station. A new, un-configured Saturn CH console looks like this:

![http://www.mediafire.com/convkey/8fb8/98nbeyn998hntc8fg.jpg](http://www.mediafire.com/convkey/8fb8/98nbeyn998hntc8fg.jpg)

From here, you can decide which products you'd like your Saturn CH to produce. Select the default station at the bottom under "Production Configuration Options" to change to another station to use as the basis of the production configuration. Only stations for sale in the Universe will be available here. For example, if you'd like the Saturn CH to produce Bofu, change the station shown to a Boron BoFu Chemical Lab. Once you're happy with your selection, select "Set production configuration". As the amount of math required to figure out what stations are required is tremendous (this script is essentially a complex calculator, as you've seen around these forums), there's a small wait (3 seconds or so). What you now see, is the requirement of stations to make a self-sustaining complex. A few notes on how the math is done:
  * Required to be a self-sustaining complex
  * Uses same race factories when possible
  * Only uses L sized mines (more efficient)
  * Minimum energy surplus is configurable. Note, that even if the minimum is set at 0, even though the SCH will endeavour to put together the lowest overkill in terms of coverage on ware production to be self sustaining, more often than not, you'll see a 104% - 120% energy coverage. This is normal, can't be avoided, and it's what you'd see with a vanilla complex, and just the way the math works, etc. As an example, if you have a big ore complex with many small cargo freighters, and you know there's going to be a shit load of jumps made, you might want to ensure that the complex is built with a minimum energy resevoir of, say, 10,000 e-cells per hour. So when configuring the station, ensure 10,000 is set in the minimum energy reservoir field. The SCH will ensure that more energy production is included in the math. You'll pay for it in terms of having to purchase more/larger SPP and their support factories, but it's your call. Don't bitch to me when your OreComplexOfMassiveness has no energy in its reservoir for your traders to jump to their destinations.. This is non-cheating, meaning the script will include more SPPs to achieve the minimum energy surplus. Sometimes a regular self sustaining complex has more energy surplus than said minimum, in which case, no extra stations above and beyond what would sustain the product ware would be required. As explain previously, energy surplus is added to the secondary resource as per regular cycle time and production. Secondary resources have absolutely no bearing on production, so don't worry if you empty it; you'll still produce.
  * Energy producing Saturn Complex Hubs ignore energy surplus (for obvious reasons).
  * Suns are taken into account for SPPs. I did the math (with help from members Smile ), to take into account suns from 50% all the way to 2000%+ in 50% increments. So you're safe.
  * The math accepts 99.85% crystal production to energy cell production as acceptable and self-sustaining. It's a minor fudge that will save you a few credits per year.

Here's an example of a Saturn Complex Hub 020, configured for 1 MJ shields:

![http://www.mediafire.com/convkey/faca/35o5m68k9lo1viwfg.jpg](http://www.mediafire.com/convkey/faca/35o5m68k9lo1viwfg.jpg)

Before we move on, here's a description of some important elements of this screen:

---

**Reset production configuration:** Goes back to the previous screen, to re-set the product of the Saturn CH. This command is unavailable if the Saturn Complex Hub contains installed stations. Also, as all of the products will be removed from the station on a production configuration reset, a docked TL is required with adequate cargo space if there is remaining ware stock in the Saturn Complex Hub.

**Operation:** Toggle this to change the operation when you select the rows in the third pane down. Either to "Install" the stations in a docked TL cargo hold into the Saturn Complex Hub, or "Remove" the stations from the hub back into the TL.
Source TL: This is the docked TL.

**Engage:** You can't see it now, but once you've installed all stations and asteroids, this command becomes available. Once selected, it starts the production of the station, and the installation panel is hidden (below).

**Production Configuration:** This shows you what's going to be produced once the Saturn Complex Hub is engaged, how long the production cycle, how many per cycle, how many per hour (hr), which resources the product is based on internally, whether it's engaged or disengaged, and energy surplus. Energy surplus is calculated, just as a regular complex would have. It represents the total produced energy, minus the energy resource required. This is necessary for your traders to sell their wares while making jumps.

**Blue stations (installation panel):** This pane is the interactive panel used to install stations from your TL into the Saturn Complex Hub. Selecting a row will remove the stations from your TL, and install them into the Saturn CH. Changing the "Operation" will reverse this process.

**Purple mineral wares (installation panel):** Some of your stations require asteroids! Selecting this will bring up an asteroid selection screen. Selecting an asteroid at this point will "import" the asteroid (using built in mining drills, tractor beams, and transport devices - what do you think you paid for?). If only a fraction of the asteroid is required, the remainder will be left. Note once an asteroid is implemented, it can be placed back onto an asteroid as long as an asteroid of the same resource type exists within the same sector.

**Ware production panel:** Gives you an idea of what's going on inside your Saturn Complex Hub when it's churning out wares. Figures are listed as wares per hour. You'll note that crystal coverage is 99.58%, and apparently acceptable. That's intentional.
Extraneous Station Info: More info on stations required/installed within this hub.

---

So as stated above, you're going to have to fill your TL up with the required stations. As you can see from our example, you'd need to go and purchase, 18 Cahoona Bakery M, 18 Cattle Ranch M, 8 Crystal Fab M, an Ore Mine L, 20 Shield Prod. Facility 1 MJ, a Silicon Mine L, and 8 Solar Power Plant Ms. Maker race is important here.

**Alternatively, you can have any owned TL do the shopping for your SCH automatically. Make sure the following conditions are met:**

Enough credits at your TL's home port (Or your player account if the TL doesn't have a homebase set)

TL Sized Ship

Trade Command 1/2

Trading System Extension

(Jump Drive recommended)

**Once the required components are installed in the TL, you can select the "Shop for Saturn CH" from the Trade menu, then select the Saturn Complex Hub you would like to equip (assuring that the SCH has the required amount of money in it's account)and the TL will head off and quickly collect the required stations. Once the shopping is done, order the TL to dock at the SCH and you will be able to auto-fit the stations automatically from the SCH menu.**

Once you've picked these up, dock the TL at the Saturn Complex Hub. You can then select the blue colour items to install the stations from your TL into the hub. Next, install the asteroids (purple wares).

If everything in this pane is green, and you see the "Engage", you're ready to produce. Hit engage, and the Saturn Complex Hub will start pumping out wares.

# Move Logistics #

There's a handy station command called _move logistics_ that enables you to move all your station agents, trade report, and station settings to another station.  This is useful for when you're upgrading your SCH to a larger size.  When you have your new one setup, run the move logistics command on the old SCH, and move logistics to the new one.  All your station agents will start using the new station, station settings will be moved, and so will the trade report.  Dockware manager sources will also be moved to the new station.