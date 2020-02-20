# What is Meshtastic?

Meshtastic is a project that lets you use
inexpensive GPS mesh radios as an extensible, super long battery life mesh GPS communicator.  These radios are great for hiking, skiing, paragliding - 
essentially any hobby where you don't have reliable internet access.  Each member of your private mesh can always see the location and distance of all other
members and any text messages sent to your group chat.

The radios automatically create a mesh to forward packets as needed, so everyone in the group can receive messages from even the furthest member.  The radios
will optionally work with your phone, but no phone is required.

### Uses

* Outdoor sports where cellular coverage is limited. (Hiking, Skiing, Boating, Paragliding, Gliders etc..)
* Applications where closed source GPS communicators just won't cut it (it is easy to add features for glider pilots etc...)
* Secure long-range communication within groups without depending on cellular providers

[![Youtube video demo](desk-video-screenshot.png)](https://www.youtube.com/watch?v=WlNbMbVZlHI "Meshtastic early demo")

### Features
(Not all of these features are fully implemented yet - see below)

* Very long battery life (should be about 8 days with the beta software)
* Built in GPS and LORA radio, but we manage the radio automatically for you
* Long range - a few miles per node but each node will forward packets as needed
* Shows direction and distance to all members of your channel
* Open and extensible codebase supporting multiple hardware vendors - no lock in to one vendor
* Communication API for bluetooth devices (such as our Android app) to use the mesh
* Eventually (within a couple of months) we should have a modified version of Signal that works with this project.
 
Typical time between recharging the radios should be about eight days.
 
This project is currently pre-alpha, but if you have questions please join our chat [![Join the chat at https://gitter.im/Meshtastic/community](https://badges.gitter.im/Meshtastic/community.svg)](https://gitter.im/Meshtastic/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge).

This software is 100% open source and developed by a group of hobbyist experimenters.  No warranty is provided, if you'd like to improve it - we'd love your help.  Please post in the [chat](https://gitter.im/Meshtastic/community).  

# Update 1

* 02/20/2020 - Our first alpha release of the radio software is ready for early users.  If you'd like to try it, we'd love your feedback.  Click [here](https://github.com/geeksville/Meshtastic-esp32/blob/master/README.md) for instructions.

## Meshtastic Android app
Soon our (optional) companion Android application will be released here:

[![Download at https://play.google.com/store/apps/details?id=com.geeksville.mesh](https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png)](https://play.google.com/store/apps/details?id=com.geeksville.mesh&referrer=utm_source%3Dhomepage%26anid%3Dadmob)

If you would like to join our super bleeding-edge alpha test group for this app, we'd love to have you.  Three steps:
1. Join [this Google group](https://groups.google.com/forum/#!forum/meshtastic-alpha-testers) with the account you use in Google Play.
2. Go to this [URL](https://play.google.com/apps/testing/com.geeksville.mesh) to opt-in to the alpha test.
3. If you encounter any problems or have questions, post in our gitter chat and we'll help.

If you'd like to help with development, the source code for the Android app is [here](https://github.com/geeksville/Meshtastic-Android).

## Supported hardware
We currently support two brands of radios.  The [TTGO T-Beam](https://www.aliexpress.com/item/4000119152086.html) and the [Heltec LoRa 32](https://heltec.org/project/wifi-lora-32/).  Most users should buy the T-Beam and a 18650 battery (total cost less than $35).  Make
sure to buy the frequency range which is legal for your country.  For the USA, you should buy the 915MHz version.  Getting a version that include a screen
is optional, but highly recommended.

We don't yet distribute prebuilt binaries.  But soon (by Feb 22) we will have a file that you can easily install on your radio via USB.  Once our software is installed, all future software updates happen over bluetooth from your phone.

For a nice TTGO 3D printable case see this [design](https://www.thingiverse.com/thing:3773717) by [bsiege](https://www.thingiverse.com/bsiege).
For a nice Heltec 3D printable case see this [design](https://www.thingiverse.com/thing:3125854) by [ornotermes](https://www.thingiverse.com/ornotermes).

# Disclaimers

This project is still pretty young but moving at a pretty good pace.  Not all features are fully implemented in the current alpha builds.
Most of these problems should be solved by the beta release:

* Encryption is turned off for now
* A number of software work items have to be completed before battery life matches our measurements, currently battery life is about two days
* The current Android GUI is pretty ugly still
* The Android API needs to be documented better
* The Bluetooth API needs to be documented better 
* The mesh protocol is turned off for now, currently we only send packets one hop distant
* No one has written an iOS app yet ;-)

For more details see the [device software TODO](https://github.com/geeksville/Meshtastic-esp32/blob/master/TODO.md) or the [Android app TODO](https://github.com/geeksville/Meshtastic-Android/blob/master/TODO.md).