
# Winget useful apps

this document shows a list of useful app installable via winget for various environments

## Winget Setup

The winget command line tool is only supported on Windows 10 1709 (build 16299) or later  
In case it is not available, you can force registration by issueing the following command in PowerShell:

`Add-AppxPackage -RegisterByFamilyName -MainPackage Microsoft.DesktopAppInstaller_8wekyb3d8bbwe.`

## Winget updates


`winget upgrade --all`

## Basic environment

```
winget install 7zip.7zip
winget install Microsoft.BingWallpaper
winget install VideoLAN.VLC
winget install Notepad++.Notepad++
winget install Google.Chrome
winget install Mozilla.Firefox
winget install Microsoft.PowerToys
```

## Antivirus

```
winget install Malwarebytes.Malwarebytes
winget install ClamWin.ClamWin
winget install ESET.ESETEndpointAntivirus
winget install Bitdefender.Bitdefender
```
## Productivity

```
winget install TheDocumentFoundation.LibreOffice
geeksoftwareGmbH.PDF24Creator
```

## Media

```
winget install GIMP.GIMP
winget install HandBrake.HandBrake
winget install Inkscape.Inkscape
winget install ShareX.ShareX
```

## Gaming env

```
winget install Valve.Steam
winget install Ubisoft.Connect
winget install GOG.Galaxy
winget install Afterburner
winget install MSI.Kombustor
```

## Dev env

```
winget install WinSCP
winget install Git.Git
winget install TortoiseGit.TortoiseGit
winget install Microsoft.VisualStudioCode
winget install Anaconda.Miniconda3
winget install Microsoft.VisualStudio.2022.Community
winget install Docker.DockerDesktop
winget install Postman.Postman
winget install TortoiseSvn.TortoiseSvn
winget install Microsoft.WindowsTerminal
winget install JetBrains.IntelliJIDEA.Community
winget install JetBrains.IntelliJIDEA.PyCharm
```

## Net env

```
winget install Insecure.Nmap
winget install WinSCP
winget install fileZilla.Client
```

