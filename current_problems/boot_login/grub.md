# How to auto boot into Arch Linux with Grub

```bash
cd /etc/default && sudo nano grub
# Change GRUB_TIMEOUT=5 to GRUB_TIMEOUT=0
# Save and exit
# Update grub (command `update-grub` if you have, else:)
sudo grub-mkconfig -o /boot/grub/grub.cfg
```

More details: [Arch Wiki](https://wiki.archlinux.org/index.php/GRUB#Configuration)
Or [my short guide](https://github.com/Harito97/SetupArch/blob/lenovo/config_arch/core_config.ipynb) when setup with multi OS.
