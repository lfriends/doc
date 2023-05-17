
# Win 11 quick hacks

in this guide
- how to restore the old context menu
- How to install W11 on any machine using a modified ISO
- How to run multiple ISO from a single USB drive
- how to skip w11 minimun requirements checks (useful for VM installation)
- how to skip logon to MSFT account during setup


## Context menu

Restore old Context Menu in Windows 11


1) reg.exe add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve
2) taskkill.exe /f /im explorer.exe; explorer


Restore Modern Context menus in Windows 11

1) reg.exe delete "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}" /f
2) taskkill.exe /f /im explorer.exe; explorer


## How to install W11 on any machine using a modified ISO

this process will show how to make a modifies W11 ISO what will skill all the HW checks
and let you install W11 on (almost) any W10 compatible PC.

1. Download the W10 and W11 ISOs to your desktop
2. Mount the W10 ISO by double-clicking on it. A new drive will show up.
3. Create a new Folder on your desktop, lets call it "W11Mod"
4. Copy all the W10 ISO content to the new "W11Mod" folder
5. Unmoud the W10 ISO by right-clickng on the corersponding drive, and select "Eject"
6. Mount the W11 ISO by double-clicking on it.
7. From the W11 drive, copy the file sources\install.wim to your "W11Mod\Sources" folder (delete the older "Install.ESD" or "Install.WIM" )
8. Unmoud the W11 ISO by right-clickng on the corersponding drive, and select "Eject"

At this point you can:  

1. create an ISO from the new W11Mod folder
    1. Option #1 use the "Media Creatio Tool" to make a USB dive bootable with w10, then update the "Sources" folder.
    2. Option #2 use a software like Furon of ImgBurn to save the Folder to a bootable ISO file.
3. Use the current "W11Mod" foldeer to update the current PC
    1. **REMEBER** to turn off VBS and core isolation security on your soon-to-be-updated PC, if it is still on.  
    2. Run the setup.exe app from the "W11Mod" folder
    3. **REMEBER**  to run the installation process WITHOUT the *online assistant or updates*!


## How to run multiple ISO from a single USB drive

you can run multiple ISOs on a single USB Drive using [Ventoy](https://www.ventoy.net)

## How to install W11 on any machine (included VMs)
Using the default W11 ISO
At the installation screen prompts for confirming language to install etc,

- press Shift+F10 to open the Command prompt
- type regedit to open the registry editor.
- go to HKEY_LOCAL_MACHINE\SYSTEM\Setup
    - right-click over Setup and select New Key: LabConfig
    - in Labconfig, add 3 DWORD32 variables
        - BypassTPMCheck  -> value: 1 
        - BypassSecureBootCheck  -> value: 1 
        - BypassRamCheck  -> value: 1 



## How to skip W11 forcing to logon to MSFT during setup


### Option 1:

As the process of W11 setup gets to the INSERT MACHINE NAME screen

* disconnetct the network (by unplugging or with cmd c:\\> ipconfig /release)

On the screen, use Shift-F10 to open a command prompt window.

*   Type OOBE\BYPASSNRO and hit the Enter-key.
*   Windows will reboot and return to the "Let's connect you to a network" screen. Only this time, you may select "I don't have Internet" to skip this.
Then you select "Continue with limited setup" to then create a local account during setup.

### Option2: 

Use the email address no@thankyou.com


