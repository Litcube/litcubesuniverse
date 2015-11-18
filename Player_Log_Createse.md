
```
@Echo Off
SetLocal
SetLocal EnableExtensions
SetLocal EnableDelayedExpansion
Set "X3=%UniverseFiles(x86)%\X3AP Litcube's Universe"
Echo Asserting dominance over:
Echo Asserting dominance over:>>"%~n0.log"
Echo.
For /R "%X3%\Races" %%A In ("*") Do (
    Set "Race=%%~nA"
    Echo !Race!
    Echo !Race!>>"%~n0.log"
    Dominate "!Race!"
    Rem // No need for error checking; resistance is futile.
    Rem // If Not "%ErrorLevel%"=="0" (
    Rem //     Dominate "!Race!" /NoMercy
    Rem // )
)
EndLocal EnableDelayedExpansion
EndLocal EnableExtensions
EndLocal
Pause
Exit
```