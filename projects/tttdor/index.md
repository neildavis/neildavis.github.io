---
title: Tomy Turnin' Turbo Dashboard
description: Conversion of a Tomy Turnin' Turbo Dashboard into a Sega Out Run arcade game.
---

[<-- Back to Homepage](../../README.md)

## Introduction

It all began with a [YouTube video](https://youtu.be/r21Zfmw7moI) that led me to Circuitbeard's
[amazing project](https://circuitbeard.co.uk/2017/08/28/tomy-turnin-turbo-dashboard-outrun-arcade/)
to convert a Tomy Turnin' Turbo Dashboard toy from the 1980s into a
[Sega Out Run](https://en.wikipedia.org/wiki/Out_Run) arcade game, complete with active
electronic dashboard.

Suffice to say, this tweaked all my nostalgia senses!

## Motivation

Despite having never attempted anything remotely like this, I felt compelled to try to achieve something similar.
Thankfully, Circuitbeard was kind enough to
[document](https://circuitbeard.co.uk/2017/08/28/tomy-turnin-turbo-dashboard-outrun-arcade/)
the entire build process, so I could follow in his footsteps.

However, I wanted to do something a little different, rather than just produce an exact replica his work.
So I decided to diversify on the dashboard component. Instead of using LEDs to re-create
the original toy's mechanical dashboard, I would fit another LCD screen and use a full digital
dashboard like you find in many modern cars.

## Development

### Components

As my first retro-mod project I leaned heaviliy on
[Circuitbeard's guide](https://circuitbeard.co.uk/2017/08/28/tomy-turnin-turbo-dashboard-outrun-arcade/),
using many of the same components (excluding those used for the dashboard LEDs):

* [Raspberry Pi 3 Model B+](https://www.raspberrypi.com/products/raspberry-pi-3-model-b-plus/)
* [Picade PCB](https://thepihut.com/products/picade-controller-board) (now discontinued)
* As close a match for the [3.5" display](https://www.amazon.co.uk/gp/product/B07D49C1XJ/) (to run the game) as I could find.
* [Slim HDMI cable](https://www.amazon.co.uk/gp/product/B00S0SN1Y6/ref=ppx_yo_dt_b_asin_title_o03_s00?ie=UTF8&psc=1), although I of course I would need TWO!
* A [3W 4Ohm speaker](https://www.amazon.co.uk/gp/product/B01LN8ONG4/)
* Various [switches](https://shop.pimoroni.com/products/maker-essentials-switches-potentiometers?variant=1418793779210), potentiometers, wires etc. Hell, I even copied using an elastic band for the throttle self centering!
* I used a Pimoroni [OnOff SHIM](https://shop.pimoroni.com/products/onoff-shim?variant=41102600138) as an alternative to the Petrockblock [PowerBlock](http://www.petrockblock.com/powerblock-raspberry-pi-power-button/).

In addition, for the digital dashboard I used:

* An [Odroid C2](https://www.odroid.co.uk/hardkernel-odroid-c2-board) to run the Android version of
[RealDash](https://realdash.net/).
* The official [Odroid VU5A 5" display](https://www.hardkernel.com/shop/odroid-vu5a-5inch-hdmi-display-with-multi-touch-and-audio-capability/) to display the dashboard.
* A couple of [USB Type A extension cords](https://www.amazon.co.uk/gp/product/B01JGQA5AI/) for keyboard/mouse access to the SBCs.
* The shortest [CAT5 Ethernet Crossover Cable](https://www.amazon.co.uk/gp/product/B004WCUQVA/) I could find to connect the Rapsberry Pi and Odroid C2.

## The Results

Here is one of [four videos](https://youtube.com/playlist?list=PLQ_4oitDNP0Kvj-5Dz6GW-dXBUhQebKhl)
from my [YouTube channel](https://www.youtube.com/c/NeilsNonsense) showing the completed project:

<div style="position: relative; padding-bottom: 56.19%; clip-path: inset(2px 2px)">
<iframe style="border: 1; top: 0; left: 0; width: 100%; height: 100%; position: absolute;" 
 src="https://www.youtube.com/embed/OGrcP-dHPcw" 
 title="YouTube video player" 
 frameborder="0" 
 allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
 allowfullscreen></iframe>
</div>
