# openlybusy
This is a tool to report if you are busy on your computer. 


Checks the Microphone/Camera usage on your computer to check if you are busy. Acts as a MQTT client to disseminate your busy status to other devices.

Made for and tested on a Ubuntu 20.04 system. Other OS support soon.

# Installation:

## Dependencies:

1. Install `inotify` through `apt`:

`sudo apt install inotify-tools`

2. Have a MQTT broker running on the network. Preferably locally.

You can `sudo apt install mosquitto`

3. Clone this repo, make an env and install the pip dependencies.

# Issues:

See Issues.


## Pseudocode?
1. Check all of these:
  * mic-cam usage (this on its own is bad; if you are on a meeting and muted; someone looks at the busylight is off (because busylight is off) ; the person disturbs you
  * Meet/Teams/Zoom usage (only Teams provides an API to check if you're on a meeting yourself; only for Enterprise accounts though) THis is needed to be implemented. I would try to add Duo, WhatsApp and other apps call presence/usage as well.
  * User set variable (a software or hardware set variable which the user sets to sign that they are on a call)
2. Report to MQTT server
3. Change LED status
