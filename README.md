# KDE-Notes

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
