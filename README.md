# mpv-wrapper

This is my mpv wrapper script.  It takes a url as an argument or from the copy buffer and attempt to play it in mpv.  If mpv can't play the url, a notification is used to let you know it failed.  This is important if the script is executed via a keybinding or launched from another application.

## Configuration

Here are various configurations I use with this script.

### i3/Sway
```sh
bindsym $mod+m exec "/path/to/mpv-wrapper.sh"
```

### mako
```ini
[summary=mpv]
background-color=#520053
```

### dunst
```ini
[mpv]
    summary = "mpv"
    background = "#520053"
```

### qutebrowser
```python
config.bind('M', 'hint links spawn ~/scripts/mpv.sh {hint-url}')
```

### tuir
```sh
video/*; /path/to/mpv-wrapper.sh '%s' ; test=test -n "$DISPLAY"
```

## Background
Way back when, I used a Firefox extension to launch audio/video links in mpv until Firefox removed that functionality.  This script was a work around that I came up with and it has evolved over time.