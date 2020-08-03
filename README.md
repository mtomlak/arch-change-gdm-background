# arch-change-gdm-background

This script automates the process of setting a background image in the GNOME Display Manager 3.36
in Arch Linux (and likely in other distros with vanilla GNOME such as Gentoo).

## Warning

This script won't work with old versions of GNOME because they have a different
way of dealing with gdm settings.

It also won't work if your system is set to a custom gdm3 theme. You will have to reset to the
default configuration of gdm3 before using the script.

This tool was made specifically to work with GNOME 3.16 and higher as it now bundles all
configuration files inside a .gresource file.

If you are going to set an image file that has spaces in its file name or folders, remember to
scape them with backslashes.

For more information about changing GDM background or if you with to do it manually see 
[GDM article on ArchWiki](https://wiki.archlinux.org/index.php/GDM#Log-in_screen_background_image).

## Installation

First, you will need to install glib2 with `sudo pacman -S glib2`

Then, you can download the script with the command below:
```
wget https://raw.githubusercontent.com/mtomlak/arch-change-gdm-background/master/arch-change-gdm-background
```
And make it executable with `chmod +x arch-change-gdm-background`

## Usage

Run the script with root privileges such as `sudo ./arch-change-gdm-background /path/to/image`.

If you see a message `login image sucessfully changed`, then, when you restart gdm or reboot your
computer, your gdm background should be covered with the image you selected.

You can restore your original gdm theme any time with sudo `./arch-change-gdm-background
--restore`.

If you feel this tool was useful and want to show some appreciation to the author of 
[the original script for Ubuntu 20.04](https://github.com/thiggy01/ubuntu-20.04-change-gdm-background), 
you can donate via https://ko-fi.com/thiggy01. If you are happy about this being forked for Arch
Linux, just star this repo and follow [me](https://github.com/mtomlak) on GitHub :)

