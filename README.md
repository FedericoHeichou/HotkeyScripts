# Keyboard Hotkey Scripts
You need to paste these script inside your Linux Distro's keyboard hotkeys settings like a command.

### Open (or set on top) Telegram's Chromium's app.
Maybe you need to change "notific" with your translation of "notications" and "notification"
```bash
bash -c "a=`wmctrl -l | grep 'Telegram\|notific' | awk '{print $1}'`; if [ -z \$a ]; then echo 'chromium-browser --app-id=hadgilakbfohcfcgfbioeeehgpkopaga'; else echo 'wmctrl -a \$a -i'; fi"
```

### Type like a keyboard what you have in the clip
```bash
sh -c 'sleep 1.0; xdotool type "$(xclip -o -selection clipboard)"'
```
