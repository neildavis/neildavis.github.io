---
title: Verbot-Pi
description: Updating a 1980s era voice controlle robot with 21st century tech.
---

[<-- Back to Homepage](../../README.md)

## Introduction

## Background

The idea was to replace the 80s era electronics in the Tomy Verbot with modern technology with the aim that we can benefit in two ways:

1. The Google AIY voice assistant would recognize our spoken requests with much greater accuracy than the notoriously poor 1980s era system.
2. Gain 'smart-speaker' style AI assistant features at the same time.

The intent was to retain all of the other existing mechanical operation parts from the original toy, instead of replacing these with servos, stepper motors etc which would have been a much greater and more expensive project!

## Features

* JSON-RPC server supporting requests over HTTP
* Voice commands supported via [Google AIY Voice Kit 2.0](https://aiyprojects.withgoogle.com/voice/)
* Google Assistant enabled

## Hardware Setup

This project makes use of:

* An original [Tomy Verbot](https://www.theoldrobots.com/verbot.html) toy with functioning motor & gears.
* A [Raspberry Pi Zero W](https://www.raspberrypi.com/products/raspberry-pi-zero-w/). The newer [Pi Zero 2 W](https://www.raspberrypi.com/products/raspberry-pi-zero-2-w/) would be a worthwhile upgrade but has not been tested.
* The 'Voice Bonnnet' and LED button from the [Google AIY Voice Kit 2.0](https://aiyprojects.withgoogle.com/voice/) Note: the complete kit also includes a Pi Zero W
* A [Pololu DRV8835 Dual Motor Driver Kit for Raspberry Pi](https://www.pololu.com/product/2753)
* A [GeeekPi Raspberry Pi GPIO Expansion Board](https://smile.amazon.co.uk/gp/product/B08C4P66HV/)
* Some (very small) [speakers](https://www.amazon.co.uk/sourcing-map-Replacement-Loudspeaker-20mmx30mm/dp/B07LGH4L4J)
* A [Pimoroni OnOff SHIM](https://shop.pimoroni.com/products/onoff-shim) (or similar smart power off solution for the Pi)
* (Optional) a 5V rechargable power source. (e.g. [a USB power bank](https://www.amazon.co.uk/%E3%80%902-Pack%E3%80%91-Miady-Portable-High-Speed-Compatible/dp/B08T1JCXR5?th=1) or similar)

## Software

All of the code required to drive Verbot and Google AIY is in my
[Verbot-Pi](https://github.com/neildavis/verbot-pi) repo which also contains more technical
information on how Verbot's original mechanical components (motors & gears) are interfaced
with the Rapsberry Pi.

## Results

So far I haven't mad a YouTube video of this project, but here is an
[Instagram Reel](https://www.instagram.com/reel/Cr6MtOzoYPi/)
of a fun demonstration I made some time ago.

<div style="position: relative; padding-bottom: 56.19%; clip-path: inset(2px 2px)">
<iframe style="border: 1; top: 0; left: 0; width: 100%; height: 100%; position: absolute;" 
 src="https://www.instagram.com/reel/Cr6MtOzoYPi/" 
 title="Instagram Reel" 
 frameborder="0" 
 allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
 allowfullscreen></iframe>
</div>
