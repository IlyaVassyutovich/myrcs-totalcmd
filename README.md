# TotalCommander (R) Configuration files

```powershell
$TCAppDataPath = Join-Path ([Environment]::GetFolderPath('ApplicationData')) "GHISLER"
$TCConfigPath = Join-Path (Get-Location) "inis"
New-SymbolicLink `
    -LinkValue (Join-Path $TCAppDataPath "wincmd.ini") `
    -TargetPath (Join-Path $TCConfigPath "root.ini")
New-SymbolicLink `
    -LinkValue (Join-Path $TCAppDataPath "sections") `
    -TargetPath (Join-Path $TCConfigPath "sections")
Write-Host "Done" -ForegroundColor Green
```