# Signal Targeted #

A long wanted feature by scripters, and a feature that has seen many diffrent implementations in the past. LU includes `[SIGNAL_TARGETED]` (since version 1.3.0)

`[SIGNAL_TARGETED]` functions the same way as standard game signals and can be regsitered as both a global signal, and a local signal. The signal itself has a 3 seccond internal re-fire delay, meaning if a fleet of 100 ships target a single ship at the same time, only one signal will fire rather then 100.

The signal is fired when `!fight.attack.object` is called, any script that provides a custom fight script that does not reference the standard `!fight.attack.object` will not fire the signal unless modified to do so.

examples:
```
[THIS]->add secondary signal: signal=[SIGNAL_TARGETED], script='my.signal.targeted', prio=0, name='my.signal.targeted'
```
```
global secondary signal map: add signal=[SIGNAL_TARGETED] race=null class=[Ship] script='my.global.signal.targeted' prio=0 name='my.global.signal.targeted'
```

Supported Objects:
  * Ship (of any kind)
  * Station (of any kind)