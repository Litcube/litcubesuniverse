# Local Variables #

In the standard X3AP Game the following objects supported script local variables:
  * Ship
  * Station
  * Sector (Since Version 2.5)

In LU (Since version 1.3.2) the following objects support local variables:
  * Ship
  * Station
  * Sector
  * Asteroid/Debris
  * Gate
  * Race (Since version 1.3.3)

In LU 1.3.3 Race objects gained support for local variables, example:
```
 $Race = [Argon]
 $Race->set local variable: name='test' value=42
 $Value = $Race->get local variable: name='test'
 write to player logbook $Value

 Output:
     42
```