# Prepare Your X3AP install for LU #

  1. Ensure you have a clean install of X3AP. A clean install is one that:
    * Is updated to the latest version of X3AP.
    * Has never had any mod/script installed to it or any mod tool associated with it. _This is key._ Mod tools like plugin manager will break your install and you can never be completely sure that previously installed mods/scripts have had every file associated with them removed or reverted to the vanilla version. When in doubt, delete your entire installation folder and reinstall from scratch.
  1. Create an install of X3AP separate from the one downloaded from steam.
    1. Find the folder your game is installed in. For a fresh X3AP install, this is located within your steam folder in ...\Steam\SteamApps\common\x3 terran conflict.
    1. Copy the 'x3 terran conflict' folder to another location. In my install I used 'C:\X3', but any location not associated with steam will do.
    1. Download the NoSteam executable from the [Egosoft website](http://www.egosoft.com/download/x3ap/bonus_en.php) and extract it to your new 'x3 terran conflict' folder.
    1. Update any shortcuts you use to point to the NoSteam exe.
  1. Ensure X3AP is set to use English localization.
    1. Create a shortcut to the NoSteam executable you just extracted.
    1. Right click on the shortcut and click properties.
    1. On the _Shortcut_ tab, locate the _Target_ text box.
    1. Paste _-language 44_ at the end of the current contents of that text box.
      * For example, the _Target_ line for my shortcut reads _"C:\X3\X3AP\_n.exe" -language 44_