# MTG Life Counter
Four player life counter for *Magic: The Gathering*

## Features

- Up to four players
- Supported life totals of -999 to 9999
- Each player can track commander damage from the other three players
- Selectable starting life of 20 or 40 (who plays paper Brawl?)
- "Roll" button for randomly selecting the starting player

## Hardware

- Arduino Nano (ATmega328)
- 4x common cathode 4-digit 7-segment displays
- 4x SP4T rotary switches
- 10x 12mm tactile switches
- 2x 74HC595 for segment driving
- 2x TPIC6B595 for sinking digit current
- 3x 74HC151 for switch and button scanning
- Passives (incl. 3 resistor networks)

## Operating Instructions

#### Power and Reset

1. Plug a mini USB cable into the Arduino and set the power switch to ON
2. The display will initialize to the starting life total selected by the starting life switch.
3. At any time, you can press the yellow reset button to clear the counters and set them to the starting value
4. You can also press both buttons near an individual display simultaneously to reset just that counter
5. To turn off the display, move the power switch to the OFF position or unplug the USB cable. The Arduino will remain powered if the USB cable is plugged in.

#### Using the Counters

1. 

#### Roll Button

The ROLL button on the counter allows you to quickly and easily select a player at random, useful for determining which player starts, or even for randomly selecting which player you should deal damage to.

To activate this feature, press and hold the blue ROLL button in the middle of the counter. When you are ready, release the button, and the random output will be shown on the displays. It will automatically disappear after a few seconds.

##### Random Number Generation

While the button is held, a counter is continuously incremented. When the button is released, the value of this counter is used to calculate which player won the roll. This counter increments approximately 64,000 times per second, roughly once every 16 microseconds. It is virtually impossible for a human to actuate the button quickly enough or precisely enough to influence the output of the roll.

##  Next Hardware Revision

List of features and fixes that will be included in the next hardware revision

- Add 30 as an option in the staring life selector
- No digital out on A6 and A7 on Nano
- Remove resistor to ground on power switch