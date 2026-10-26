# USB notification sound

Plays a sound when a USB device is connected or disconnected.

| File | Install to |
|---|---|
| `100-usb.rules` | `/etc/udev/rules.d/` |
| `usb-insert.service` | `/etc/systemd/system/` |
| `usb-remove.service` | `/etc/systemd/system/` |
| `USB-Insert.wav` | `/etc/sounds/` |
| `USB-Remove.wav` | `/etc/sounds/` |

In both `.service` files, replace `{user}` with your username.
They also assume UID 1000 (`XDG_RUNTIME_DIR=/run/user/1000`); change it if yours differs (`id -u`).

After copying:

```
sudo systemctl daemon-reload && sudo udevadm control --reload
```
