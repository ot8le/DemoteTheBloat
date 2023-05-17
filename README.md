## Debloat Windows 11

### Powershell (admin):

#### Remove all preinstalled Microsoft apps (can be redownloaded again through the store):

```powershell
Get-AppxPackage -AllUsers | Remove-AppxPackage
```

#### Add back Microsoft store:

```powershell
Get-AppxPackage -allusers Microsoft.WindowsStore | Foreach {Add-AppxPackage -DisableDevelopmentMode -Register "$($_.InstallLocation)\AppXManifest.xml"}
```

## Compress Windows 11

### Command Prompt (admin):

#### Enable the built in CompactOS feature:

```cmd
Compact.exe /CompactOS:always
```
