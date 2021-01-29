## Configuration files for the Wayland Display Protocol

Wayland is a display server protocol. It is aimed to become the successor of the X Window System. 

Display servers using the Wayland protocol are called compositors because they also act as compositing window managers (for example, sway).
If you want to learn more about wayland, you can read the [wayland arch wiki](https://wiki.archlinux.org/index.php/Wayland).

### What does this repo include?
It includes the configuration files for the wayland programs I use. If you want check my configs for zsh, vim, git, etc... 
You should check that repo: 

### How to install this configuration?
This repo uses the [gnu stow](https://www.gnu.org/software/stow/) as a dependency (yeah, I know that an script that does the symlink would do the job, but working with stow is easier).

For installing stow in arch linux, it is in the standard repos so:

        $ sudo pacman -S stow

Once you have stow installed, clone this repo and execute stow

        $ git clone
        
        $ cd wayland-config
        
        $ stow * 

### List of programs used for this repository and its X11 "equivalent"

| Program                  | xorg     | wayland      |
| ------------------------ | -------- | ------------ |
| window manager           | dwm      | sway         |
| notification daemon      | dunst    | mako         |
| clipboard manager        | xclip    | wl-clipboard |
| menu                     | dmenu    | wofi         |
| screenshot tool          | memo     | grim         |
| adjust color temperature | redshift | gammastep    |

