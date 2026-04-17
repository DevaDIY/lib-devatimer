# DevaTimer

DevaTimer is a simple non-blocking timer library for Arduino and ESP32.

Created by Deva DIY  
Website: https://devadiy.com

## Features
- setInterval()
- setTimeout()
- changeInterval()
- pause() / resume()
- isActive()
- isPaused()
- remove()

## Why DevaTimer?
DevaTimer helps you run multiple timed tasks without using delay().

## Installation
1. Download this library
2. Put it in Arduino/libraries
3. Restart Arduino IDE

## Example
```cpp
#include <DevaTimer.h>

DevaTimer ledTimer;

void setup() {
  pinMode(2, OUTPUT);

  ledTimer.setInterval(1000, []() {
    digitalWrite(2, !digitalRead(2));
  });
}

void loop() {
  ledTimer.update();
}