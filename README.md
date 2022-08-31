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
I make a gamepad controller that's used in my
[After Burner](projects/ab/index.md) project.

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
