# Primary Objects #

Each EMS mission has a primary object or location, also known as the "focal point" of the mission. The purpose of the focal point is to create a sphere in space that the mission is active within, for the rest of this article this shall be called the 'sphere of influence'.

In all cases with only one exception, the mission will have a sphere of influence around the focal point set to the mission writers desired size in meters, the size of the sphere can be set with the _icdm.mission.set.displayrange_ script. If the display range is set to 0, the mission will never receive either EVENT\_ON\_PLAYER\_ENTER\_AREA/EVENT\_ON\_PLAYER\_LEAVE\_AREA events nor will the mission show up on the right side mission overlay.

The following Focal Points support a Sphere of Influence:
  * Ship/Station
  * Positional Array (X, Y, Z, Sector)

There is one more focal point type that has no sphere of influence, that is a Sector - if a sector is set as the primary object, and the mission has a display range of at least 1, the mission shall be visible across the entire sector. If the display range is set to 0 the mission shall remain invisible.

The following script can be used to set a missions primary object:
```
 = [THIS]->call script 'icdm.mission.set.primaryobj' : targetMission=$Mission primaryObject=$Object
```

If the primaryObject argument is null, the current primary object will be removed from the mission. It is recommended that a mission always have a valid primary object.

# Primary Object Events #
If the missions primary object is a Ship or a Station, two events can fire in relation to what happens to the primary object.
(for information about event arguments, see **[Script Event List](EMS_Tut_Events.md)**)
  * EVENT\_PRIMARYOBJECT\_LOST
> > The PRIMARYOBJECT\_LOST event is fired whenever the primary object is either killed, bails or is borded.

  * EVENT\_PRIMARYOBJECT\_CHANGESECTOR
> > The PRIMARYOBJECT\_CHANGESECTOR event fires whenever the primary object moves from sector to sector, this is only relevant for Ships flying through gates. This will not fire if you set the primary object manually to an object or location in another sector.