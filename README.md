# Linux Usability Problems

This is a curated list of all Linux usability problems on distros intended for the average user: 

- Debian derivatives
- Fedora
- Solus

 # Global
  - GNOME:
    - Activities Overview
      - Right click should show a contextual menu, not open the app
      - Middle click should close, not open app
    - Middle click on every panel should start a new instance
    - Tray icon should be re-added
      - Workaround: KStatusNotifierItem/AppIndicator Support extension for GNOME
  - Wine
    - Drawing tablets still not work after 11 years, wintab32.dll needs to be fixed
      - Workaround: try to set wintab32.dll as native, but it will probably not work
  - Xorg
    - Chrome still has screen tearing in 2019...
      - Workaround: chrome://flags/ and enable `Override software rendering list`
  - GTK File Picker
    - https://gitlab.gnome.org/GNOME/gtk/issues/233
      - The issue about the GTK file picker not having thumbnails is 15 years that is open
      - Workaround: none with vanilla distro
      - Deepin and KDE use a modified GTK version, that's why thumbnails are shown there

 # Fedora 30
  - Fonts:
    - Japanese language doesn't show in Chrome
    - Emojies don't show in Chrome
  - EGL-Wayland:
    - GNOME:
      - Rarely crashes with NVIDIA forcing a logout and returning to GDM3
      - GNOME doesn't honor `GTK_WIN_POS_CENTER`, GTK windows that are set to be centered on screen aren't actually centered
      
# Debian 10
  - Nouveau:
    - EGL-Wayland:
      - Mouse lags
      - Keyboard lags


