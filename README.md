# MultiStepper & AccelStepper Libraries

This is the Arduino MultiStepper & AccelStepper library. It provides an object-oriented interface for 2, 3 or 4 pin stepper motors and motor drivers. The standard Arduino IDE includes the Stepper library (http://arduino.cc/en/Reference/Stepper) for stepper motors. It is perfectly adequate for simple, single motor applications.

AccelStepper significantly improves on the standard Arduino Stepper library in several ways:

* Supports acceleration and deceleration
* Supports multiple simultaneous steppers, with independent concurrent stepping on each stepper
* API functions never delay() or block
* Supports 2, 3 and 4 wire steppers, plus 3 and 4 wire half steppers.
* Supports alternate stepping functions to enable support of AFMotor (http://github.com/adafruit/Adafruit-Motor-Shield-library)
* Supports stepper drivers such as the Sparkfun EasyDriver (based on 3967 driver chip)
* Very slow speeds are supported
* Extensive API
* Subclass support

### Support

Example Arduino programs are included to show the main modes of use.

You can also find online help and discussion at http://groups.google.com/group/accelstepper Please use that group for all questions and discussions on this topic. Do not contact the author directly, unless it is to discuss commercial licensing. Before asking a question or reporting a bug, please read

* http://en.wikipedia.org/wiki/Wikipedia:Reference_desk/How_to_ask_a_software_question
* http://www.catb.org/esr/faqs/smart-questions.html
* http://www.chiark.greenend.org.uk/~shgtatham/bugs.html

### Compatibility

Tested on Arduino Diecimila and Mega with arduino-0018 & arduino-0021 on OpenSuSE 11.1 and avr-libc-1.6.1-1.15, cross-avr-binutils-2.19-9.1, cross-avr-gcc-4.1.3_20080612-26.5. Tested on Teensy http://www.pjrc.com/teensy including Teensy 3.1 built using Arduino IDE 1.0.5 with teensyduino addon 1.18 and later.

### Changelog [Differences from Core Repo]

In this repo, some additional features was added to the core repository. This features can explainable as `size()` and `get()` methods.

`size()` method returns total filled size of multiple AccelSteppers array to caller function.

```C
uint8_t MultiStepper::size()
{
    return _num_steppers;
}
```

`get()` method return selected stepper to caller function from multiple AccelSteppers array.

```C
AccelStepper& MultiStepper::get(uint8_t item)
{
    return *_steppers[item];
}

```

### Author

This is a Github mirror of the AccelStepper source code from http://www.airspayce.com/mikem/arduino/AccelStepper/ This software is Copyright (C) 2008 Mike McCauley. It is provided under the GNU GPL 2.0 license.

---

###### Improved by Berk Altun - www.vberkaltun.com

