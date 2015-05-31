# i3 Window Manager Config File.
## This is my configuration for [i3 Window Manager](http://i3wm.org/)

### Instalation
Just clone this repository into ~/.i3 folder.
```
git clone https://github.com/alexandremello/i3-cofig.git ~/.i3
```

### Some personalizations:
- Removed arrow keys mappins
- Moved motion keys to vim style (hjkl)
- Shutdown menu
- Add `Layout mode` to move around the selected window
- Add suport to multimedia keys:
  - volume up
  - volume down
  - play/pause
  - prior
  - next

### Dependencies
  - `consolekit` package is needed for shutdown and restart

### Issues
If you get `Error org.freedesktop.UPower.GeneralError: not authorized` error for hibernate, try to enable the hibernation:

#### for Ubuntu:
Edit or create the `/etc/polkit-1/localauthority/50-local.d/com.ubuntu.enable-hibernate.pkla` file with this content:
```
[Re-enable hibernate by default]
Identity=unix-user:*
Action=org.freedesktop.upower.hibernate
ResultActive=yes
```
