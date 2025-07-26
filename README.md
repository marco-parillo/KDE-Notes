# KDE-Notes

## Falkon Spell-Checking

```
$ git clone https://chromium.googlesource.com/chromium/deps/hunspell_dictionaries
$ cd hunspell_dictionaries/
$ ls -l en-US*
-rw-rw-r-- 1 mparillo mparillo 451968 Dec  7 07:21 en-US-10-1.bdic
$ cd /usr/share/qt5/
$ sudo mkdir qtwebengine_dictionaries
$ cd qtwebengine_dictionaries
$ sudo cp $HOME/hunspell_dictionaries/en-US-10-1.bdic .
```

## Start Kate with an empty document
There is a checkbox on the welcome page at the bottom to turn it off.

The setting is also to be found in: Settings --> Configure Kate --> Session
and the setting is a check box named "Show welcome view for new windows"

[Hat-tip](https://www.reddit.com/r/kde/comments/zy2alp/i_dislike_the_new_way_kate_opens_a_welcome_screen/).

## Clean Plasma Cache
Deleting all things with "plasma" in the name from ~/.cache then restarting.

## If your Plasma/X11 looks *YUGE*
```
sudo vim /etc/sddm.conf
i
[X11]
ServerArguments=-nolisten tcp -dpi 96
escape
:wq
```
## Surface 3 Wi-Fi
```
sudo vim /etc/NetworkManager/conf.d/default-wifi-powersave-on.conf
```
By default there is:
```
[connection]
wifi.powersave = 3
```
Change the value to 2.
[Hat-tip](https://unix.stackexchange.com/questions/269661/how-to-turn-off-wireless-power-management-permanently).

## Firefox

### To use KDialog in Firefox

```
sudo /etc/profile.d/mozilla-common.sh
i
export GTK_USE_PORTAL=1
escape
:wq
```
Or try:
* Enter about:config in the URL Bar
* Set widget.use-xdg-desktop-portal.file-picker=1

### Cursor icon changes in Firefox

You may need to create the directories first before you:
```
sudo vim /usr/share/icons/default/index.theme
i
[Icon Theme]
Inherits=Oxygen_Yellow
```
If you don't know your cursor theme name, they are listed in:
```
$ find /usr/share/icons ~/.local/share/icons ~/.icons -type d -name "cursors"
```
