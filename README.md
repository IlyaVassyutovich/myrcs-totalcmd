# TotalCommander (R) Configuration files

```powershell
$TCAppDataPath = "c:\Users\ilya.vassyutovich\AppData\Roaming\GHISLER\"
$TCConfigPath = "M:\ilya.vassyutovich\documents\myrcs-totalcmd\inis"
New-SymbolicLink `
    -LinkValue (Join-Path $TCAppDataPath "wincmd.ini") `
    -TargetPath (Join-Path $TCConfigPath "root.ini")
New-SymbolicLink `
    -LinkValue (Join-Path $TCAppDataPath "sections") `
    -TargetPath (Join-Path $TCConfigPath "sections")
Write-Host "Done" -ForegroundColor Green
```