# W10-AntiCat
## Disable Narrator and Magnifier for Windows 10
Run CMD.exe under elevated prompt

Take owner of Narrator.exe and Magnify.exe

```
takeown /A /F "%WINDIR%\System32\Narrator.exe"
takeown /A /F "%WINDIR%\System32\Magnify.exe"
```
Deny everyone execute them
```
icacls "%WINDIR%\System32\Narrator.exe" /deny *S-1-1-0:(X)
icacls "%WINDIR%\System32\Magnify.exe" /deny *S-1-1-0:(X)
```
Done!
