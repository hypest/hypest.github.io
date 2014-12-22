---
layout: post
title: "New project: Power usage monitor"
modified:
categories: blog
share: true
excerpt:
tags: []
image:
  feature:
date: 2014-12-22T03:25:00+02:00
---

It has been bugging me for some time now...

## Some background

My obsession with collecting data from my surroundings is nothing new. I once set out to build a web service to collect all my purchases and produce charts I could draw budget conclusions from. Even though that project did its circle (not a particularly successful one), it just cannot get out of my mind and might be revived in some future ;)

This time around, my attention is at something more simple (hopefully): collecting power usage data at our home. Specifically, I wanted to start monitoring some of the major power consumption culprits, the washing machine and the tumble dryer.

My attitude has changed through the years: I now try to focus as much as possible to the area of the "problem", the solution of which will bring in good value, fast. So, focusing only at the big white appliances that their usage can generally be optimized, such as the washer and the dryer. A counter example is the fridge... there isn't much you can do to your habits to lower its consumption!

## What went OK

The project basically started back in August 2014, when I created a Google Form to help me and my wife to easily log in the data.

<figure>
  <img src="{{ site.url }}/assets/images/googleform_washes.png" alt="Google Form for the washes input"/>
  <figcaption>Google Form for the washes input</figcaption>
</figure>

The data was gathered by manually reading the display of the watt-meter I already had in my gadgetset:

<figure>
  <img src="{{ site.url }}/assets/images/Multifunctional_Mini_Ammeter_D02A.jpg" alt="The D02A watt-meter I had looked much like this one"/>
  <figcaption>The D02A watt-meter I had looked much like this one</figcaption>
</figure>

The project was working perfectly. We were logging in the reading after every wash, zero the meter out and switch plugging in the dryer, let it do the drying circle and then log the reading in again. Life was good! After a couple of months, we already had a good picture of how we use those two appliances.

## Reality check

And then disaster... the meter's display stopped functioning :(

We had to bring the project back to working condition though. Our usage pattern was about to change (a newborn child was just around the corner!) and the meter would help us re-optimize. I did replace the meter, going a step further this time:

<figure>
  <img src="{{ site.url }}/assets/images/FHT-9998_L1.jpg" alt="The FHT-9998 wireless watt-meter"/>
  <figcaption>The FHT-9998 wireless watt-meter</figcaption>
</figure>

Yeap, I went wireless! I chose to pick up these 433MHz power monitors (with their including display unit) as I saw the opportunity to move away from the manual gathering of the readings and perhaps manage to do that automatically, using some form of receiver. A nice detail: the package already had 2 independent monitoring sockets included, so there was no need to switch which appliance was plugged it anymore.

And then reality kicked in... The baby joined us and every project of mine was put on hold, including resuming the consumption monitoring procedure. The baby arriving meant all our brainpower was focused on its well-being; we didn't have the patience to put in the extra work of gathering the readings anymore!

A new solution had to be put in place, and the plausible alternative I could think of was to try that idea and do the data gathering automatically.

## Stop thinking; start doing

So, here's the plan:

 * Use my RaspberryPi, its nice chips of which are only collecting dust and cosmic radiation at the moment
 * Get a 433MHz receiver
 * Manage to pick up the signals emitted by the 2 watt-meters
 * Collect the data into some database
 * Show some nice tables and charts of the data

And that's how I got to today's breakthrough: I ordered the receiver! Woohoo!

<figure>
  <img src="{{ site.url }}/assets/images/sdr-usb-dongle.jpg" alt="The RTL2832U based SDR receiver dongle"/>
  <figcaption>The RTL2832U based SDR receiver dongle</figcaption>
</figure>

The dongle is marketed as a DVB-T TV tuner but with Software Defined Radio (SDR) capabilities. The preliminary research I did showed that I will probably be able to setup the raspi to use the dongle and "wire" it through some software packages to decode the signals. Let's see. This is me, trying to move the project one step further, even if that step will be an experiment.

Hacks are always an experiment anyway ;)
