# Keyboard Hotkey Scripts
You need to paste these scripts inside your Linux Distro's keyboard hotkeys settings like a command.<br>
Then maybe you need to terminate your session and login again.

### Open (or set on top) Telegram Chromium's app.
Maybe you need to change "notific" with your translation of "notications" and "notification"
```bash
bash -c "a=`wmctrl -l | grep 'Telegram\|notific' | awk '{print $1}'`; if [ -z \$a ]; then chromium-browser --app-id=hadgilakbfohcfcgfbioeeehgpkopaga; else wmctrl -a \$a -i; fi"
```

### Type like a keyboard what you have in the clip
```bash
sh -c 'sleep 1.0; xdotool type "$(xclip -o -selection clipboard)"'
```

### For mouse (using .xbindkeysrc of xbindkey package)
```bash
"xdotool key ctrl+alt+Right"
  b:8

"xdotool key ctrl+alt+Left"
  b:9
```
