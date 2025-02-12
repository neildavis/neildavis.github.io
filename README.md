# Welcome

Here you will find links to my various projects and some articles
about them.

## Retro-Mod'ing

I love to take old hardware, usually from the 80s or 90s, and use
modern technology like SBCs & MCUs to convert them into something
unimaginable in their original lifetime.

### Tiger / Grandstand After Burner Tabletop Arcade Conversion

Can I convert an old LCD based tabletop game to play the full Sega arcade original?
Find out [here](projects/ab/index.md)

### Verbot-Pi

The idea was to replace the 80s era electronics in the Tomy Verbot with modern technology
to improve on the poor voice recognition of the original toy. 
As a bonus we gain AIY Google Voice Assistant capabilities!

Beyond voice recognition, the intent was to retain all of the other existing mechanical operation parts from the original toy, instead of replacing these with servos, stepper motors etc which would have been a much greater and more expensive project!

Find out more [here](projects/verbotpi/index.md)

### Tomy Turnin' Turbo Dashboard - Out Run & RealDash Conversion

My first retro-mod. After inspiration from [Circuitbeard](https://github.com/circuitbeard),
I converted a Tomy Turnin' Turbo Dashboard toy from the 1980s to play Sega's Out Run
arcade classic!

More details [here](projects/tttdor/index.md)

## Embedded & Microcontroller Stuff

Modern microcontrollers are such fun to work with.
Controlling external hardware & electronics from software is so cool.
I like to hack things up on these using C, C++, Python and [Go](https://tinygo.org/).

I'm also a contributor to the [TinyGo Drivers](https://github.com/tinygo-org/drivers)
repository, where I have contributed code for infrared receivers, stepper motor drivers
and more.

### Raspberry Pi Pico (RP2040) meets TinyGo

In [this repo](https://github.com/neildavis/pi_pico_tinygo_examples) I experiment
in coding for the [RP2040](https://www.raspberrypi.com/products/rp2040/) MCU using
[TinyGo](https://tinygo.org/) - A Go Compiler For Small Places.

The main focus is reproducing the builds from an old
[Elegoo Arduino Uno R3 Kit](https://github.com/neildavis/pi_pico_tinygo_examples/tree/main/elegoo_most_complete_starter_kit)
on a [Raspberry Pi Pico](https://www.raspberrypi.com/products/raspberry-pi-pico/).

### USB HID Gamepad

[CircuitPython](https://circuitpython.org/) makes creating
[USB HID](https://en.wikipedia.org/wiki/USB_human_interface_device_class)
devices easy!

In [this repo](https://github.com/neildavis/teensy_hid_gamepad)
I make a gamepad controller that's used (amongst others) in my
[After Burner](projects/ab/index.md) project.

## Raspberry Pi Stuff

### Linux / RPi USB HID & ALSA integration

With the deprecation of Pimoroni's [Picade PCB](https://www.adafruit.com/product/2708)
I was left with a need for alternative hardware to fill it's place.
The main requirements were:

* Digital AND Analog game controller inputs
* Audio amplification for small speakers
* Volume control inputs

Controller inputs were fulfilled using various microcontrollers to act as USB HID controllers
like my [Teensy HID gamepad](https://github.com/neildavis/teensy_hid_gamepad)

Separate I2S audio amplifier boards were available, but the missing component was a way
to control the volume from physical inputs like buttons.

I modified my USB HID gamepad
code to send the  'Consumer Control' volume events much the same way as USB keyboards do.
Whilst this worked on Desktop Linux OSs like RPi OS, it didn't work on the 'Lite' versions
of the OS that I typically use in my Retro mod projects. 

Something was missing, so I developed
[this daemon](https://github.com/neildavis/alsa_volume_from_usb_hid) to overcome this problem.

### TM1637 4 x 7-Segment LED display driver for Raspberry Pi

I needed a driver for this simple device on the Raspberry Pi. Having not found a good usable version
I decided to write one myself to 'bit bang' the protocol described in the component's datasheet
using the RPi's GPIO pins.

Many GPIO based drivers like this require a particular GPIO library, of which there are several,
e.g. [wiringPi](https://github.com/WiringPi/WiringPi),
[pigpio](http://abyz.me.uk/rpi/pigpio/) &
[libgpiod](https://git.kernel.org/pub/scm/libs/libgpiod/libgpiod.git/)

For convenience I decided to develop my driver 'agnostic' to any underlying GPIO library.
This was a fun way to learn about
[dynamic library loading](https://tldp.org/HOWTO/Program-Library-HOWTO/dl-libraries.html)
under Linux whilst relieving clients of a build-time link dependency on any particular 
GPIO library.

More details and source are available in [this repo](https://github.com/neildavis/lib_tm1637_rpi)

[](https://github.com/neildavis/lib_tm1637_rpi)

## iOS Stuff

### JSON-RPC Proxy

A [JSON-RPC 2.0](https://www.jsonrpc.org/specification)
proxy for protocols in Swift & Objective-C.

Write RPC function declarations in Swift or Objective-C using native types.
The proxy will create the JSON-RPC request payload object,
and convert the JSON-RPC response into a callback via a block/closure,
marshalling all parameter and return types between Objective-C/Swift & JSON automagically.

The [examples](https://github.com/neildavis/json-rpc-proxy/tree/main/Examples/RandomLottery)
demonstrate use of the proxy in Swift to create
[FRP](https://en.wikipedia.org/wiki/Functional_reactive_programming) constructs using
[RxSwift](https://github.com/ReactiveX/RxSwift) and Apple's
[Combine](https://developer.apple.com/documentation/combine) framework.

Sound cool? Find out more [here](https://github.com/neildavis/json-rpc-proxy)

## Amiga stuff

There has been a resurgence of interest in 'Retro' consoles & Computers recently.
I was inspired to retrieve my old [Commodore Amiga A500+](https://en.wikipedia.org/wiki/Amiga)
from my parents' atic and see if it still worked. 

It didn't, but after a [Refurb/Rebuild project](https://www.instagram.com/reel/CzQ4ar6osu_/)
I was able to do some fun things with it:

### Amiga A500 Keyboard Tester

As part of the refurb I needed to test the keyboard controller, so I developed this little
[Arduino based utility](https://github.com/neildavis/amiga_keyboard_tester)
to be sure my keyboard was working correctly.

### Amiga ASM Development Workflow

With working hardware I decided I wanted a taste of Amiga game development from 'back in the day.' 
Despite many advances that now allow Amiga development to be performed on modern PCs and OSs, 
I found there was a lack of automated workflows, particularly under Linux.

During development of my game I developed a [GNU Make](https://www.gnu.org/software/make/)
based workflow to integrate various tools into an end-to-end automated CI/CD pipleline.
It made sense to open source this aspect of the project so I created 
[this repo](https://github.com/neildavis/amiga_asmdev_workflow) to demonstrate it's use
on a small demo application with the aim of sharing it with other members of the Amiga dev community.

### Riviera '79 / AmiGameJam 2024

I decided to port Sega's 1979 'Monaco GP' arcade game to the Amiga, since it never received an
official port. Since I was already working with Ben Geeves on his
[PC remake](http://forum.arcadecontrols.com/index.php?topic=134445.0)
of the same game I could reuse graphical and audio components after some conversion.

The end result is [Riviera '79](https://nngaming.itch.io/riviera-79)
which was entered into the AmiGameJam 2024 competition.

<div style="position: relative; padding-bottom: 56.19%; clip-path: inset(2px 2px)">
<iframe style="border: 1; top: 0; left: 0; width: 100%; height: 100%; position: absolute;" 
 src="https://www.youtube.com/embed/TT05mwjG4GM" 
 title="YouTube video player" 
 frameborder="0" 
 allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
 allowfullscreen></iframe>
</div>
