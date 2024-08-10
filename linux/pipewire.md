https://linuxgenie.net/install-pipewire-debian-12/
https://wiki.debian.org/PipeWire

sudo apt update
sudo apt install pipewire-audio wireplumber pipewire-pulse pipewire-alsa libspa-0.2-bluetooth
pipewire --version
systemctl --user --now enable wireplumber.service
systemctl --user --now disable wireplumber.service (OPTIONAL)
wireplumber --version
sudo reboot
