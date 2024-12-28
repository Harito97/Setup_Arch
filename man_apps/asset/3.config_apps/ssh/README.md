# How to setup SSH server on Arch Linux

All refer to [this](https://linuxconfig.org/linux-setup-ssh).

1. Install openssh
```bash
sudo pacman -S openssh
sudo pacman -S ufw
```

2. Start the sshd service
```bash
sudo systemctl start sshd
```

3. Enable the sshd service
```bash
sudo systemctl enable sshd
```

4. Check the status of the sshd service
```bash
sudo systemctl status sshd
```

5. Allow the ssh service through the firewall with a specific port
```bash
#sudo ufw allow ssh
sudo ufw allow 97
```

6. Check the status of the firewall
```bash
sudo ufw status
```

7. Connect to the server
```bash
ssh username@ip_address
ssh -p 22 username@ip_address   # default port is 22
ssh -p 97 username@ip_address # specific port is 97
# to check ip address
ip a
# or
hostname -I
```

8. Done
```

[]: # (END)
