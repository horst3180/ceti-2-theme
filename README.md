Ceti-3.14 is the official continuation of Ceti for Gnome 3.14. It has been completely revamped and is now based on Vertex. 

A Chrome/Chromium theme is included.

Requirements: gnome-themes-standard package for the GTK3 theme. Murrine and pixbuf engines for the GTK2 theme.

Bug reports are appreciated.

###########################
#      Requirements       #
###########################

* Gnome 3.14
* GTK3: gnome-themes-standard package or a package which contains the adwaita engine
* GTK2: Murrine engine and pixbuf engine

Please search in the repositories of your distribution because the package names vary from distro to distro.

###########################
#      Installation       #
###########################
The extracted zip file contains two different subfolders: "Ceti-3.14" (Gtk and Gnome Shell theme) and "Chrome" (Theme for Chrome/Chromium).
Install the theme by copying "Ceti-3.14" to /usr/share/themes

If necessary set the right permissions:

    sudo chmod -R 755 /usr/share/themes/Ceti-3.14


To set the theme, run the following commands:

    gsettings set org.gnome.desktop.interface gtk-theme "Ceti-3.14"
    gsettings set org.gnome.desktop.wm.preferences theme "Ceti-3.14"
    gsettings set org.gnome.shell.extensions.user-theme name "Ceti-3.14"

Instead of applying the theme with the gsettings commands you can select them in Gnome Tweak Tool like any other theme.

To install the Chrome/Chromium theme open the "Chrome" folder in the extracted archive and drag and drop the Ceti-3.14-chrome.crx file into the Chrome/Chromium window. The source of the Chrome themes is located in the source "Chrome/source" folder.

#######################
#   Troubleshooting   #
#######################

If the metacity theme doesn't show up in gnome-tweak-tool copy the theme folder with only the metacity theme inside to ~/.local/share/themes. Otherwise gnome-tweak-tool won't find the metacity theme. (This shouldn't happen if you copy the theme to /usr/share/themes)

If you experience Gnome-Shell crashes, replace the "gnome-shell.css" file in the "Ceti-3.14/gnome-shell/" folder with the "gnome-shell-no-crash.css" file

