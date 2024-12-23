# How to auto start Hyprland (my Desktop Enviroment) when login without display manager

I read this information from [Hyprland wiki](https://wiki.hyprland.org/0.18.0beta/Getting-Started/Quick-start/).
```After you have installed Hyprland, you can either launch it from a TTY with Hyprland or from a login manager.```
In my case, I don't use any display manager (login manager), so I will start my DE from a TTY after login with command `Hyprland`.

But what if we want to auto start Hyprland from a TTY after login, I see this [Arch Wiki](https://wiki.archlinux.org/title/Hyprland) in 3.2 Auto login.
```
Users can automatically login by using a display manager or adapting the method described in Xinit#Autostart X at login.
```
As Xinit - as I know - used by X11, so I think it's not suitable for Wayland. So use display manager is the best way to auto start Hyprland.
Or you can read the below section.

# How to auto start a command or script when login

There are many ways to auto start a command or script when login.
Here are some of them, however, I think use systemd is a better way!

```bash
# add script to /etc/profile.d
# Eg: I create a autostart.sh will auto execute after login
cd /etc/profile.d
sudo nano autostart.sh
# define what you want to do
sudo chmod +x autostart.sh
```
