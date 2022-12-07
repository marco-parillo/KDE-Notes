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
## To use KDialog in Firefox
```
sudo /etc/profile.d/mozilla-common.sh
i
export GTK_USE_PORTAL=1
escape
:wq
```
