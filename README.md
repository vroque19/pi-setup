# pi-setup
how to setup rpi

# tailscale

1. install tailscale onto rpi
2. enable tailscale and ssh `$ sudo tailscale up --ssh`
3. check status with `$ sudo tailscale status`
4. enable ssh in system preferences 
  > preferences -> interfaces -> SSH
5. on main computer tailscale dashboard, edit ACL tags for rpi and add server tag to rpi
6. sudo reboot
7. test ssh from dashboard

# VNC
1. enable ssh in system preferences (probably enable everything)
  > preferences -> interfaces -> VNC
2. `$ sudo reboot`
3. `$ sudo systemctl status wayvnc`



# code tunnel
1. install vscode on rpi
2. run `$ code tunnel # sign into github`
3. copy and paste into `$ code tunnel rename <newname>`
4. place service file at `/etc/systemd/system/<servicename>.service`
5. change permissions to allow for execution `$ sudo chmod a+wrx <servicefilname>`
6. `$ sudo systemctl enable <servicefilename>`
7. `$ sudo systemctl start <servicefilename>`
8. `$ sudo reboot`
