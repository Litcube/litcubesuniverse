# Bounce #

Bounce helps keep ships from running into things.

## I've Heard of This Before! ##

As you may be aware from the Egosoft forums, Bounce was a script package that helped alleviate some of the frustration caused by default ship behaviour.  Ships in vanilla would run headlong into an opposing capital ship to uphold their honour in a misguided tribute to you, the Emperor.  However, this fucking sucked.

So I made Bounce.  It was a very, very complicated script package that did a few things.  Firstly, if a ship was too close to another ship, it would do a 180 and fly away.  Secondly, if there were no enemies about, it would make ships invincible, so they wouldn't run into asteroids.  This shit all sounds simple, but it was difficult.  To attain the dimensions of where and when a ship should do that 180, users needed a wall file.  That was a process, and a true test of intelligence for the EgoSoft community (few passed).  It didn't work as perfectly as I would have hoped for a lot of people.  Mainly because people can't read, but also because I don't write very well, and the process was cumbersome.

## Shut Up, Litcube.  What Is Bounce in LU? ##

Bounce in LU is simpler for you, the player.  It's on by default in the game options menu.  There's a few differences between the old script one and this one.  The biggest, is that LU Bounce is **only** a system where ships will turn around when about to collide, and that's all it does.  Here are some others:

  * The old Bounce uses scripts.  LU Bounce does not.
  * The old Bounce guessed where to fly if it was about to have a collision.  The LU bounce uses an ancient Persian magic called _mathematics_ to ascertain the trajectory in which it should travel.  You'll see far less collisions this way.
  * Bounce now works on AI ships as well as player ships.
  * The thing where the old bounce would make your ships invincible when there were no enemies in sight, that thing doesn't happen anymore.  There's no invincible bullshit anymore.
  * Bounce is faster.  You can turn it off if you're a dipshit, but essentially, there's negligible performance impact.