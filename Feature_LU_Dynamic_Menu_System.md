# Litcube's Universe Dynamic Menu System #


Vanilla script menus have delays, and new sub menus flash the underlying background (often the command console) between menus.  Also, updating data is usually via a "fresh" or "update" option in the script.

Some strides were made to implement direct manipulation of the menu array through running a background script.  This is a little tedious and still poses limitations.

No longer.  All (if not, most) of Litcube's Universe scripts implement the new LU Dynamic Menu System, allowing you, the scripter, to make menus that look and feel just like hard coded menus.  Sub menus won't flash the background, they'r snappy, they offer more control, and they update data real time (with a 1 sec refresh rate to keep performance in check).

Several new script commands were implemented to support this feature, as well as new implementations of the underlying mechanics of how script menus work.  For examples, see the Litcube's Universe menus that start with "Menu.".  There's always a pair.

**Menu._X_:**  The launcher<br>
<b>Menu.<i>X</i>.SM:</b> The <i>set menu</i> sister.  She is called every second.