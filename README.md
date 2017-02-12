# Fluxbox dotfiles


# Fluxbox configuration

## What is this?
Configuration for fluxbox window manager. The files included here normally reside in admin users home directory `~/.fluxbox`. 

Fluxbox is a lightning fast window manager which is very good suited for running on 
* home servers (in case you need a browser or window applications there) 
* internet servers, accessible via [nomachine VNC](http://www.keycruncher.com/blog/2008/07/07/vnc-vs-nomachine-nx-nomachine-wins-hands-down/) or [XRDP Server](http://networkstatic.net/xrdp-an-easy-remote-desktop-setup-for-your-ubuntu-servers/)
* small hardware like Rasperry PIs

Some features which really make fun since this stuff is so fast:
* Moving windows between workspaces (Drag Drop or via keys)


## Prerequisites
On debian-like systems without desktop environment ("Ubuntu Server", `debootstrap`-systems), the installation of xorg server and fluxbox is < 400MB in size:

```
apt-get install -y xorg fluxbox rxvt-unicode-256color qalculate grun xfe
```
this installs following executables:

* `startx`: start x server and fluxbox under current user's context
* `rxvt`: terminal emulator with unicode support
* `qalculate`: cool calculator
* `grun`: application starter better then the built-in `fbrun`
* `xfe`: simple file manager with 3 panes

## Todo
* configure 
	* window handling keys for local screen `WIN-<key>`: mix of 
		* windows resizing behaviour
		* WIN-xxx app start (WIN-r, WIN-e)
	* workspace handling keys 
		* MacOS workspace switching Control-<left>,<right> 
	* window <> workspace handling: move windows between workspace
* add apple keyboard switch script to menu and system
* add xrdp server
* add help text for keyboard shortcuts, onscreen desplay on `start` workspace like
```
/usr/bin/wterm -tr -fn  "-misc-*-medium-r-*-*-10-*-*-*-*-*-*-*" -fg grey +sb -e cat /dev/xconsole &
```

