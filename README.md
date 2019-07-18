# Linux Usability Problems

This is a curated list of all Linux usability problems on distros intended for the average user: 

- Debian derivatives
- Fedora
- Solus

# Contributing

Use a hierarchical style, from low level to high level if the OS stack is relevant, or to add more detail to the usability problem, example:

- NVIDIA GPU
  - Nouveau
    - Xorg
      - XFCE
        - etc...


# Global
 
 - GTK File Picker
   - https://gitlab.gnome.org/GNOME/gtk/issues/233
     - The issue about the GTK file picker not having thumbnails is 15 years that is open
     - Back in the day I remember of how a photographer wouldn't use Linux only for this problem, he couldn't see the thumbnails of the photos he had to upload
     - Workaround: none with vanilla distro
     - Deepin and KDE use a modified GTK version, that's why thumbnails are shown there
 - Freedesktop.org
   - File associations:
     - `xdg-open`,`exo-open`,etc..
       - `xdg-open` doesn't have a standard to open a folder where a file is contained and select that file
         - Solution: extend xdg-open or create a new modern standard
       - File associations are a mess, there isn't a standard on where and how they are saved
   - `.desktop` files can't run binaries with Exec or TryExec but only shell scripts
      - Workaround: use a proxy shell script to run the exe, still pretty stupid in 2019
 - Password prompt for sudo operations should be optional and replaced with a [YES/NO] dialog like on Windows with UAC
   - Solution: During install a user can choose if to keep the password dialog or the messagebox dialog
 - GNOME:
   - Screenshot tool icon should show by default on the top bar
     - There is a lot of space, it's small, and very useful
   - Show minimize, maximize and close buttons all on the right right a sane UI
     - Workaround: enable this using GNOME Tweaks
   - Activities Overview
     - Right click should show a contextual menu, not open the app
     - Middle click should close, not open app
   - Middle click on app icons on every panel should start a new instance
   - Right clicking the clock should show Time/Date settings, not open it
   - Tray icon should be re-added
     - Workaround: KStatusNotifierItem/AppIndicator Support extension for GNOME
 - Wine
   - Drawing tablets still not work after 11 years, wintab32.dll needs to be fixed
     - It's pointless to have a Platinum running photoshop if drawing tablets are broken
     - Confirmed that Huion tablets DO NOT WORK AT ALL with Wine
     - Workaround: try to set wintab32.dll as native, but it will probably not work
 - NVIDIA
    - nouveau and non-free drivers
      - Xorg
        - Chrome
          - Screen tearing in 2019...
            - Workarounds: 
              - chrome://flags/ and enable `Override software rendering list`, works often
              - Distros should purge Xorg and use https://github.com/NVIDIA/egl-wayland
 - The software install window both on Debian and Fedora show "License: Proprietary" when installing local packages


# Fedora 30
 - Fonts:
   - Japanese language doesn't show in Chrome
   - Emojies don't show in Chrome
   - Sometimes on a clean install fonts on terminal are distorted???
 - EGL-Wayland:
   - GNOME:
     - Rarely crashes with NVIDIA forcing a logout and returning to GDM3
     - GNOME doesn't honor `GTK_WIN_POS_CENTER`, GTK windows that are set to be centered on screen aren't actually centered

# Debian 10
 - NVIDIA 980Ti
   - Nouveau:
     - (EGL?)-Wayland:
       - Mouse lags
       - Keyboard lags


