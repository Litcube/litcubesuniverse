# Registering EIs #

**_STRONGLY_** recommend using X-Studio with these instructions.

If your mod has globals or other data that needs to be exported or imported using LU's system, read this thing.

There's three scripts you'll have to copy:

setup.EI.Template<br>
Z.EmpireCopy.Template.Export<br>
Z.EmpireCopy.Template.Import<br><br>

Copy the files.  <i>Template</i> in these files should be renamed to a name that will be consistent with your mods name.  For example, we'll name it <i>JouXMissions</i>.  Your files will now be named:<br>
<br>
setup.EI.JouXMissions<br>
Z.EmpireCopy.JouXMissions.Export<br>
Z.EmpireCopy.JouXMissions.Import<br><br>

<h2>Setup Script</h2>

Now open up the setup script.  As it says in the template, change the three arguments of the script.<br>
<br>
<b>Name:</b> The name we picked.  In this example, it's JouXMissions.<br>
<b>FileNumber:</b>  A filename for the export.  LU uses 8382.  Use something higher than 8390.<br>
<b>PageNumber:</b>  Use an unused page number.  Somewhere between 8005 and 80100 should do.<br>

Now, when a player loads a game, that setup script will register your two renamed scripts with the LU EI engine.  Whenever a player export his game or imports his game those two scripts will be run.<br>
<br>
<h2>Export Script</h2>

Open up the Export script you made.  You can edit everything between those two "=======" lines.<br>
<br>
This script writes.  It writes to the file and page you specified in the setup script.<br>
<br>
There's two examples in there.  The first is a simple single variable export.  Anything before a gosub Line: call will write the $Text variable.  $Text can be of any data type, but objects (ships, stations, asteroids, sectors) will not work right.  In this case, we're writing the string 'Joubarbe Likes Cats' to the file.<br>
<br>
The second example is an array write.  That script is a motherfucker of an acheivement.  That one line will write any array in any structure with any number of dimensions.  One line.  Remember again, though, that objects can't be written right.<br>
<br>
If you need to write an object, get creative.  For a sector, don't write the sector object, write its X and Y coordinates, and then read them back in when you get to the import script.<br>
<br>
Refer to the LUV export script for reference.<br>
<br>
<h2>Import Script</h2>

Open up the Import script you made.  As with the export, edit only between those two double lines.<br>
<br>
Import obviously needs to be read in the same order as it was exported.<br>
<br>
Here, there's two examples that will read what was written in the example exports.<br>
<br>
The first will read the next line into $Text.  This $Text in the example happens to be 'Joubarbe Likes cats'.  When you make a gosub Line: call, the line is read into $Text.<br>
<br>
The second will read our exported array into the variable $Return.