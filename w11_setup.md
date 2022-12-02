
# Win 11 quick hacks

## Context menu

Restore old Context Menu in Windows 11


1) reg.exe add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve
2) taskkill.exe /f /im explorer.exe; explorer


Restore Modern Context menus in Windows 11

1) reg.exe delete "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}" /f
2) taskkill.exe /f /im explorer.exe; explorer


---
## How to install W11 on any machine (included VMs)

At the installation screen prompts for confirming language to install etc,

- press Shift+F10 to open the Command prompt
- type regedit to open the registry editor.
- go to HKEY_LOCAL_MACHINE\SYSTEM\Setup
    - right-click over Setup and select New Key: LabConfig
    - in Labconfig, add 3 DWORD32 variables
        - BypassTPMCheck  -> value: 1 
        - BypassSecureBootCheck  -> value: 1 
        - BypassRamCheck  -> value: 1 


---
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


