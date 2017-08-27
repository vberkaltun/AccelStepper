# MultiStepper & AccelStepper Libraries

This is the **extended** Arduino MultiStepper & AccelStepper library. It provides an object-oriented interface for 2, 3 or 4 pin stepper motors and motor drivers. The standard Arduino IDE includes the Stepper library (http://arduino.cc/en/Reference/Stepper) for stepper motors. It is perfectly adequate for simple, single motor applications.

### Compatibility

Tested on Arduino Uno and Arduino Mega with using Arduino IDE 1.8.0 or later version. In additional to this, You can learn all compatibility informations from http://www.airspayce.com/mikem/arduino/AccelStepper/ as up-to-date.

### Changelog [Differences from Core Repo]

In this repo, some additional features was added to the core repository. This features can explainable as `size()` and `get()` methods.

`size()` method returns total filled size of multiple AccelSteppers array to caller function.

```C
uint8_t MultiStepper::size()
{
    return _num_steppers;
}
```

`get()` method returns selected stepper to caller function from multiple AccelSteppers array.

```C
AccelStepper& MultiStepper::get(uint8_t item)
{
    return *_steppers[item];
}

```

### Author

This is a Github mirror of the AccelStepper source code from http://www.airspayce.com/mikem/arduino/AccelStepper/ This software is Copyright (C) 2008 Mike McCauley. It is provided under the GNU GPL 2.0 license.

###### Improved by Berk Altun - www.vberkaltun.com

