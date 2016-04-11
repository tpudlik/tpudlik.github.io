---
layout: page
excerpt: "Raspberry Pi remote control for the AC."
title: RaspAC
tags: [Raspberry Pi, IR remote, AC remote]
image:
  feature: header-RPiAC.jpg
---

During the 2013/2014 academic year I lived in sweltering Durham, North
Carolina.  [My apartment][] had air-source heat pumps with IR remotes, but the
remotes' range was very short, and by the time I found myself close enough to
the AC unit it was too late to turn it on&mdash;I was  already (sweating) in
my living room!  Wouldn't it be more useful to turn the AC on before I leave
work?

Solution: I purchased a Raspberry Pi, installed an Apache web server,
[connected some IR diodes and a receiver](http://upverter.com/alexbain/f24516375cfae8b9/Open-Source-Universal-Remote/),
[set up the Linux Infrared Remote Control library](http://alexba.in/blog/2013/01/06/setting-up-lirc-on-the-raspberrypi/),
[recorded the IR codes](http://absurdlycertain.blogspot.com/2013/03/lirc-raspi-remote-control-configuration.html),
and voilà!  I can SSH into my air conditioner.

But SSH is not the most user-friendly way of interacting with a
server&mdash;particularly from a mobile device.  So I hosted a web app on my
Pi which allowed me to submit commands to the heat pump and displayed the
latest readings from the [temperature sensor][].  Since I moved out of North
Carolina the app is no longer online, but you can play with a
[mockup hosted on Google App Engine][mockup] (username Guest, password Guest). Or check out [the source on GitHub](https://github.com/tpudlik/RaspAC).

I tried setting up a system for controlling the other two heat pumps in my
apartment through the same web server.  The other pumps are in  different
rooms, so IR signals couldn't be sent directly from the Pi.  My plan was to
use a network of [Moteinos][], low-power Arduino clones with built-in wireless
(RF) transceivers.  The Pi would communicate with the Moteinos via a [RF
transmitter][], and these would send IR codes to the heat pumps in their
rooms.  I got this system working, but the Moteinos couldn't drive enough
current from their logic pins through an IR diode to communicate with the AC
unit from a good distance.  I moved out of North Carolina before I solved
this issue!

<!-- <figure>
    <a href="{{ site.url }}/images/RPiAC.jpg"><img src="{{ site.url }}/images/RPiAC.jpg"/></a>
    <figcaption>A Raspberry Pi IR transceiver.</figcaption>
</figure> -->

[My apartment]: http://www.universityapartmentsdurham.com/
[temperature sensor]: http://www.adafruit.com/products/385
[mockup]: http://raspac-mockup.appspot.com/
[Moteinos]: http://lowpowerlab.com/moteino/
[RF transmitter]: http://www.ebay.com/itm/1pcs-RF-transmitter-and-receiver-kit-for-Arduino-project-433Mhz/370685120131?rt=nc
