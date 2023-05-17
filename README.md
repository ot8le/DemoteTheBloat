## Debloat Windows 11

### Powershell (Admin):

#### Remove all preinstalled Microsoft apps (can be redownloaded again through the store):

```powershell
Get-AppxPackage -AllUsers | Remove-AppxPackage
```

#### Add back Microsoft store:

```powershell
Get-AppxPackage -allusers Microsoft.WindowsStore | Foreach {Add-AppxPackage -DisableDevelopmentMode -Register "$($_.InstallLocation)\AppXManifest.xml"}
```

<hr>

## Compress Windows 11

### Command Prompt (Admin):

#### Enable the built in CompactOS feature:

```cmd
Compact.exe /CompactOS:always
```

### File Explorer (NTFS Drives):

1. Secondary click and select <strong>Properties</strong>.
2. Check the box that says <strong>Compress this drive to save disk space</strong>.
