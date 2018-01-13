# README

## About

This is a theme and configuration that tries to match the Windows XP look more closely on Linux. It is currently optimized for XFCE version 4.12.

If you use another desktop environment, `xfdesktop` should work most effectively.

[Screenshots](https://zumipap.deviantart.com/art/Windows-XFCE-725338933)

* XP GTK theme based on : [WinXP-themes](https://github.com/B00merang-Project/WinXP-themes)

* XP Icons based on : [WinXP-Icons](https://github.com/B00merang-Project/WinXP-Icons)

* Other icons included:
    - [Classic95](https://www.gnome-look.org/content/show.php/Classic95?content=157298)

    - [w2k-bibo](http://linux.softpedia.com/get/Desktop-Environment/Icons/w2k-bibo-49820.shtml)

## Installing this theme

Download the zip file by clicking `Clone or Download` -> `Download ZIP`. Extract it to a directory of your choosing. This extracted folder will be known as "repo".

Locations prefixed with `~/` indicate an item or folder in your *home directory*.

### Setup

If you're using `xfwm4`, under Window Manager Tweaks, disable everything except "Show shadows under popup window".

You may choose to disable compositing altogether in favor of another compositor such as `compton` or `xcompmgr`.

### Copy files

1. From repo, copy the `Windows XP Luna` folder in `gtk-themes` into your local themes folder (in `~/.themes/` or `~/.local/share/themes/`)

2. Copy the contents of the `icons` folder in repo to the `~/.icons/` folder

3. Copy `configs/fonts.conf` in repo to the `~/.config/fontconfig/` folder.

4. Open a terminal and type in:

    ```ln -s ~/.config/fontconfig/fonts.conf ~/.fonts.conf```

5. Copy `configs/gtkrc-2.0` in repo to `~/.gtkrc-2.0`.

6. Copy `configs/compton.conf` in repo to the `~/.config/` folder if you use `compton`.

7. Copy the contents of the `panel-bgs` folder in repo to a folder called `~/.xfce-panel-bgs` (or any name you want)

### Copy fonts

1. If you have Windows installed on a virtual or physical machine, obtain the Trebuchet, Tahoma, and Microsoft Sans Serif fonts. Copy the font files to your computer and install them. To ease this process, install [font-manager](https://fontmanager.github.io/).

2. If you do not have a Windows installation near you, do the following:

    - Install the Microsoft core fonts. (`ttf-mscorefonts-installer ` on Ubuntu)

    - Obtain the Tahoma font by running [this script](https://gist.github.com/maxwelleite/913b6775e4e408daa904566eb375b090).

    -  Get the Microsoft Sans Serif font somewhere from the internet and install it.

### Styling
Using your appearance customizer,(`lxappearance`, XFCE4 appearance settings etc.) perform the following:

1. Set the font to "Tahoma", size 8.

2. Switch the widget style to "Windows XP Luna".

3. Do the same thing with the window manager/window decoration. For the font (if possible), set it to "Trebuchet MS Bold", size 10, title aligned to the left.

4. Set icons theme to "WinXP".

5. On the desktop, set the icon size to 32.

Additionally, 

1. Set the main panel height to 30.

2. Use the `panel-setup.png` image in repo to help you set up the panel if you're using XFCE.

3. Notifs should have the maximum icon size of 16px.

You should have a setup that looks the closest to a generic PC setup from the mid 2000's. Full cloak mode!

## Office 2007 theme

In the `gtk-themes` folder, there is also an MS Office 2007 theme for use in LibreOffice versions 5 and up. If you want to use this theme, copy it to `/usr/share/themes`. You may need root privileges.

It is made for the new "MUFFIN" interface / ribbon interface. To enable it, go to Options -> LibreOffice -> Advanced. Click the "experimental features" checkbox and restart LibreOffice.

In the View menu there should be options for a "Notebookbar". Select the "Tabbed" option. After that, go to View -> Toolbar Layout -> Notebookbar to activate the ribbon-like layout.

To use this theme, create a new script containing the following:

```
#!/bin/bash

env SAL_USE_VCLPLUGIN=gtk GTK2_RC_FILES=/usr/share/themes/Office 2007/gtk-2.0/gtkrc" /usr/bin/libreoffice "$@"
```

`$HOME/.themes/` points to your local themes direcory. You may change it to `$HOME/.local/share/themes/` if your local themes directory is there instead.

Save the script to `/usr/bin/libreoffice-2007`, you may need root privileges.

In a root terminal, run `chmod +x /usr/bin/libreoffice-2007` to make it executable.

After that, you may need to update all of your LibreOffice shortcuts (changing `libreoffice` to `libreoffice-2007`) to reflect the new script.