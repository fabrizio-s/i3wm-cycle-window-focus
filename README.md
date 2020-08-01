### cycle_window_focus.py ###

The i3wm commands 'focus right' and 'focus left' change the window focus to the next/previous window, even if that window is in some other workspace on another monitor.

This script allows to cycle focus **only** through the windows in the **currently focused workspace**.

To focus the next window in the current workspace:

```
$ python cycle_window_focus.py
```

To focus the previous window in the current workspace:

```
$ python cycle_window_focus.py -p
```

If the script is bound to some key combination (such as $mod+Alt) in the i3wm config file in the following way:

```
bindsym $mod+Tab exec ~/.i3/cycle_window_focus.py
```

then the script should be granted executable permissions:

```
$ chmod +x ~/.i3/cycle_window_focus.py 
```

### Requirements ###

- Python (only tested with version **3.8.5**+)
- i3ipc, which can be installed on Arch Linux with:

```
$ sudo pacman -S python-i3ipc
```


