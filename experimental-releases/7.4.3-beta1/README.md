# Hermes Lite 2 — Ethernet Recovery 7.4.3 Beta 1

*Experimental firmware for HL2 operators interested in remote operation.*

## Why I developed this firmware

I'm preparing to operate my Hermes Lite 2 remotely.

During testing, I discovered that a brief interruption of the Ethernet connection could leave the radio unreachable. The HL2 was still powered on, but Thetis could no longer communicate with it. Restoring operation sometimes required restarting the radio.

That's inconvenient when the radio is nearby. When it's at a remote location, it can mean making a trip just to turn the radio off and back on.

**My goal is to allow the HL2 to recover from these interruptions automatically whenever possible.**

## What does Beta 1 do?

Beta 1 improves how the HL2 recovers from certain Ethernet interruptions.

When the physical Ethernet connection is restored, the firmware makes a fresh attempt to obtain a network address. It also allows more time for a slow router, switch, or DHCP server to become available after a power interruption.

The goal is simple: **restore communication with the radio without requiring a trip to the remote site.**

## Does it work?

In my testing with a real Hermes Lite 2, Thetis, Ethernet switches, and a DHCP server, the modified firmware successfully recovered from several network interruptions without having to restart the radio.

The results are encouraging, but Beta 1 is still experimental and has not been tested with every network configuration.

## Will it solve every remote-connection problem?

No.

It can help with certain physical Ethernet interruptions and with network recovery following a power failure at a remote site, once the equipment is powered and operating again. It cannot restore a failed Internet connection or equipment that remains offline.

If the radio has already switched to its fallback network address, it may still require intervention to reconnect through a different network.

## Should I try it?

If you have experienced similar recovery problems related to Ethernet interruptions or power glitches, and are comfortable installing and restoring HL2 firmware, your testing and observations would be welcome.

Please retain a copy of your currently working firmware before installing Beta 1.

Because this is experimental firmware, it may help, but relying on it as the only recovery method for an unattended remote station is not a good idea.

**If it saves you a trip to the remote site, it has served its purpose.**

This is not an official firmware release. It is not intended to replace the official HL2 firmware or imply that our approach is preferable for every installation.

For technical design details and timing qualifications, see the separate `HL2_7.4.3_Beta1_Technical_Review.pdf` paper.

73,

Dalton, W5EIM
