https://forums.debian.net/viewtopic.php?t=155520

**os debian 12 testing kde Wayland Pipewire**
I installed an usb bluetooth adapter and had troubles conning devices. When I added a new device I got the error "br-connection-profile-unavailable". I added a phone, pc and headpohne. They all gave the same error.

After I long search (google) I found the solution:
- install libspa-0.2-bluetooth
- reboot
And then bluetooth worked.

I checked another pc with and there was libspa-0.2-bluetooth installed allready. I don't know why libspa-0.2-bluetooth was missing on my pc.

**Curious. KDE in Bookworm has Pulseaudio as default, not Pipewire.**
libspa-0.2-bluetooth is the bluetooth module for Pipewire however.


**Installing libspa-0.2-bluetooth,**
that in turn required the installation of 3 more packages, 
finely fixed some conflict between bluetooth and pulseaudio 
on my Thinkpad laptop with Debian 12 that made hard to switch between internal and bluetooth speakers.
