---
layout: post
title: "Temperature monitor with RTL-SDR"
modified:
categories: blog
share: true
excerpt:
tags: []
ogimage: assets/images/temps-hypest-org.jpg
image:
  feature:
date: 2015-2-13T15:40:00+02:00
---

So, after taking its time travelling the eastern oceans, my [RTL2832U based DVB dongle][dvbdongle] finally arrived this week! Check [the previous post]({% post_url /blog/2014-12-22-sdr-dongle-ordered %}) for some background on what I have in mind for it ;)

In the short time with it, I only had partial success picking up the energy monitor sensor values. Some signal seems to picked up but can't decode and ectract the values just yet. But, I did managed to have quite some fun with the RF temperature sensors I have lying around!

Here's a nice shot of a little page I've put up, showing the temperature history at my balcony:
<figure>
  <img src="{{ site.url }}/assets/images/temps-hypest-org.png" alt="History of outside temperature at my balcony"/>
  <figcaption>History of outside temperature at my balcony</figcaption>
</figure>

Here's the basic architecture of the setup:

 * The DVB dongle is plugged into a RasperryPi
 * The Raspi is connected to my LAN and runs the rtl_433 utility, modified by me to be able to decode the values of each sensor
 * When picked up, the temperature value gets submitted to a Google form, storing the value in a Google Sheet
 * In the Sheet, the history of temperatures is displayed on a chart
 * Bonus action: upon submitting a new value, a script in the Sheet sends an email to [ifttt.com][ifttt], activating a recipe that tweets the value! Check out the [Twitter feed][twitterfeed]! The feed is rate-limited to roughly 1 tweet every 30mins.

rpi stuff
=========

##### compile and install rtl-sdr

##### compile and install rtl_433

##### play with rtl_433 to decypher the signals

# google form+sheet stuff

# twitter stuff

# temps.hypest.org stuff

[dvbdongle]: http://www.ebay.com/itm/201140299234
[ifttt]: http://ifttt.com
[twitterfeed]: https://twitter.com/hypestTemp
