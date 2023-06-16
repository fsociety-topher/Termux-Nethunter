# Termux-Nethunter
### Source : David Bombal
1. Termux Apk
- https://github.com/termux/termux-app/releases
2. Update & Upgradde 
- apt update -y
- apt upgrade -y
3. Storage Permission
- termux-setup-storage
4. Wget
- apt install wget -y
5. Nethunter Installation
- wget -O install-nethunter-termux https://offs.ec/2MceZWr
- chmod +x install-nethunter-termux
- Choose 1 if you dont nethunter zip file 
- or download in 
6. Nethunter 
- to open type - $ nh
- set up Kex passwd - $ nethunter kex passwd
- to run Kex - kex &
9. Nethunter Store 
- https://store.nethunter.com/en/
- download and install 
10 Nethunter Kex 
- after install search in store - Nethunter Kex
- allow storage 
- type the passwprd of kex created 
- connect 
---
# Phantom Process Killer
### Source Ksk Royal

1. What is Phantom Process killer
- For those who don’t know, what the heck is  a phantom process killer in android 12 and  
13? It’s a background process limiter that kills  the app processes using excessive CPU or system  
resources. Let's say the parent app started  spawning a child processes of more than 32,  
if they are found to be using an excessive CPU,  the phantom process killer kicks in and kills  
the entire app Hierarchy. This happens without  the consent of the user and the app gets killed  
automatically and creating a problem for the  end-user experience. TERMUX is a well-known  
app suffering from this background limitation.This is  kinda annoying and it prevents you  
from running Linux operating system  on a non-rooted android device.
2. Fix Phantom Process killer
- Enable USB Debugging
  - About Phone -> Build Number tap 7 Times -> Developers Option -> Turn on USB Debugging
- Connect Device To Computer
  - Allow USB Debugging
- Download SDK Tool
  - https://developer.android.com/tools/releases/platform-tools
  - after extract
- Open ADB
  - highlights the address bar at the top and copy it
  - Go go window search bar and search "environment variable"
  - open and click "Environment Variable" at downdown
  - in Second Column choose "path" and click edit
  - click new and paste the location This allows  
access to the ADB command throughout  the system.
  - open Command prompt and type adb device This  
means the computer can interact with  Android devices using the ADB shell.
3. Paste the following in command Prompt
- adb shell "/system/bin/device_config set_sync_disabled_for_tests persistent"
- adb shell "/system/bin/device_config put activity_manager max_phantom_processes 2147483647"
- adb shell settings put global settings_enable_monitor_phantom_procs false
4. Also Recommended
- Disable Battery Restriction in Termux 

# Chromium in Termux Nethunter
1. Open Nethunter
2. nano /etc/apt/sources.list
3. apt update
4. sudo su
5. apt install chromium chromium-l10n -y
6. nano /usr/share/applications/chromium.desktop
7. locate the line "Exec=/usr/bin/chromium &U"
8. delete the &U and paste --no-sandbox
9. Open VNC kex and start uisng chromium
