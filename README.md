# Ceti-2 Theme

Ceti-2 is a theme for GTK 3, GTK 2 and Gnome-Shell. It supports GTK 3 and GTK 2 based desktop environments like Gnome, Unity, Budgie, Pantheon, etc.

Ceti-2 is the official continuation of Ceti for Gnome 3.14 and 3.16. It has been completely revamped and is now based on Vertex.

### Requirements

* Gnome/GTK 3.14 or 3.16
* The gnome-themes-standard package
* The GTK 2 murrine engine

Main distributions that meet these requirements are

* Arch Linux and Arch Linux based distros
* Ubuntu 15.04
* elementary OS Freya
* Debian Testing/Unstable
* Gentoo
* Fedora 21 and 22
* OpenSuse 13.2 and Tumbleweed

Derivatives of these distributions should work, aswell.

If your distribution is not listed, please check the requirements yourself.

### Installation

**Important:** Remove all older versions of the theme from your system before you proceed any further.

    sudo rm -rf /usr/share/themes/Ceti-2
    rm -rf ~/.local/share/themes/Ceti-2
    rm -rf ~/.themes/Ceti-2

**Manual Installation**

To build the theme you need 
* `autoconf`
* `automake`
* `pkg-config` or `pkgconfig` if you use Fedora
* `libgtk-3-dev` for Debian based distros or `gtk3-devel` for RPM based distros
* `git` if you want to clone the source directory

If your distributions doesn't ship separate development packages you just need GTK 3 instead of the `-dev` packages.

Install the theme with the following commands

**1. Get the source**

If you want to install the latest version from git, clone the repository with

    git clone https://github.com/horst3180/ceti-2-theme --depth 1 && cd ceti-2-theme

If you want to install the latest stable release, run

    git clone https://github.com/horst3180/ceti-2-theme --depth 1 && cd ceti-2-theme
    git fetch --tags
    git checkout $(git describe --tags `git rev-list --tags --max-count=1`)

or download it from https://github.com/horst3180/Ceti-2-theme/releases and cd into the extracted archive

**2. Build and install the theme**

    ./autogen.sh --prefix=/usr
    sudo make install

Other options to pass to autogen.sh are

    --disable-gnome-shell      disable GNOME Shell support
    --disable-gtk2             disable GTK2 support
    --disable-gtk3             disable GTK3 support
    --disable-metacity         disable Metacity support
    --disable-unity            disable Unity support

    --with-gnome=<version>     build the theme for a specific Gnome version (3.14, 3.16)
                               Note: Normally the correct version is detected automatically and this
                               option should not be needed.

After the installation is complete you can activate the theme with `gnome-tweak-tool` or a similar program by selecting `Ceti-2`.

**Uninstall the theme**

Run

    sudo make uninstall

from the same directory as this README resides in, or

    sudo rm -rf /usr/share/themes/Ceti-2

### Extras

The `extra` directory in the same directory as this README resides in contains a Chrome/Chromium  theme and an alternative metacity theme, which hides the window titles of maximized windows (doesn't work on Gnome 3.16).

To install the Chrome/Chromium theme go to the `extra/Chrome` folder and drag and drop the Ceti-2-chrome.crx into the Chrome/Chromium window. The source of the Chrome themes is located in the source "Chrome/source" folder.

To install the alternative metacity theme, copy the `Ceti-2-alternative-metacity` folder to `/usr/share/themes` and select it as window theme.

### Troubleshooting

If you get artifacts like black or invisible backgrounds under Unity, disable overlay scrollbars with

    gsettings set com.canonical.desktop.interface scrollbar-mode normal
====

If you experience Gnome-Shell crashes, replace the "gnome-shell.css" file in the "/usr/share/themes/Ceti-2/gnome-shell/" folder with the "gnome-shell-no-crash.css" file

    sudo mv /usr/share/themes/Ceti-2/gnome-shell/gnome-shell-no-crash.css /usr/share/themes/Ceti-2/gnome-shell/gnome-shell.css


### Bug reporting
If you find a bug, please report it at https://github.com/horst3180/Ceti-2-theme/issues

![alt tag](http://orig13.deviantart.net/08f9/f/2015/109/d/e/ceti_2_theme_by_horst3180-d8393uc.jpg)
