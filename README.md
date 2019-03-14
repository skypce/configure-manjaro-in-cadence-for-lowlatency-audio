# Configure Cadence in Manjaro Linux

Instructions for configure Cadence for Lowlatency audio in Manjaro


## Installation

Manjaro:

```sh
Open a console:
sudo pacman -S cadence jack2-dbus pulseaudio-jack
sudo usermod -a -G audio $USER
sudo nano /etc/pulse/default.pa
### Add or modify this two lines at end of file
set-default-sink jack_out
set-default-source jack_in
#Edit /etc/security/limits.conf and add the follow lines at end of file
@audio - rtprio 90          # maximum realtime priority
@audio - memlock unlimited  # maximum locked-in-memory address space (KB)
#Create a shortcut.desktop file and copy it to .config/autostart folder
sudo cp cadence.desktop $HOME/.config/autostart/
```

Configure Cadence:
Step1:
![](cadence-step1.jpg)
Step2:
![](cadence-step2.jpg)
Step:3
![](cadence-step3.jpg)

Enjoy.




## Meta

César R. Cid Méndez – [@YourTwitter](https://twitter.com/skypce) – skypce@gmail.com


