## Configuration files for the Wayland Display Protocol

Wayland is a display server protocol. It is aimed to become the successor of the X Window System. 

Display servers using the Wayland protocol are called compositors because they also act as compositing window managers (for example, sway).
If you want to learn more about wayland, you can read the [wayland arch wiki page](https://wiki.archlinux.org/index.php/Wayland).

### What does this repo include?
It includes the configuration files for the wayland programs I use. If you want check my configs for zsh, vim, git, etc... 
You should check the [main dotfiles repo](https://github.com/Pablito2020/dotfiles).

### How to install this configuration?
This repo uses the [gnu stow](https://www.gnu.org/software/stow/) as a dependency (yeah, I know that an script that does the symlink would do the job, but working with stow it's easier).

For arch linux based distros, stow is in the official repos:

        $ sudo pacman -S stow

Once you have stow installed, clone this repo and execute stow

        $ git clone https://github.com/Pablito2020/wayland-config
        
        $ cd wayland-config
        
        $ rm README.md && stow -vSt ~ * 
        

### List of programs used for this repository and its X11 "equivalent"

| Program                  | xorg     | wayland           |
| ------------------------ | -------- | ----------------- |
| window manager           | dwm      | sway              |
| window bar               | dwm      | waybar            |
| notification daemon      | dunst    | mako              |
| clipboard manager        | xclip    | wl-clipboard      |
| menu                     | dmenu    | dmenu-wayland-git |
| screenshot tool          | memo     | grim + slurp      |
| adjust color temperature | redshift | gammastep         |
| screen lock              | -        | swaylock-effects  |


### Installation of depencencies:
Install all the dependencies/packages on arch linux with the following commands:

        $ sudo pacman -S sway waybar wl-clipboard wofi grim slurp gammastep udiskie mako kitty thunar
        $ paru -S swaylock-effects dmenu-wayland-git ttf-iosevka-nerd arc-gtk-theme

You can install the default gtk theme "Orchis" [from here](https://github.com/vinceliuice/Orchis-theme).

You can install the font for swaylock [from here](https://www.dafont.com/calvin-and-hobbes.font).
