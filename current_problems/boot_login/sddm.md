# How to login without display manager

This is useful if you want to login to the terminal and start the GUI manually.

```bash
sudo systemctl disable display-manager
# Removed "/etc/systemd/system/display-manager.service".
sudo systemctl disable sddm
```

To enable it again:

- use `sudo systemctl enable sddm`
- replace `sddm` with what ever display-manager you use (eg: lightdm, sddm, gdm, gdm3, ...)
- for me, I use `sddm` as my display manager.
