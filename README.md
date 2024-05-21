# TTL_Timer
A 60 second timer with stopwatch function, start/stop button and reset capabilities; made for a year 2 university project.

![Real2](https://github.com/AndreiBertescu/TTL_Timer/assets/126001291/90a0b0da-a99b-44b2-b295-82790008a7b8)

## Description and features
- There are three buttons:
  - A <strong>START_STOP</strong> button, wich pauses and unpauses, with the help of a JK flip-flop, the main timer.
  - A <strong>RESET</strong> button, wich resets both the timer and the lap time.
  - A <strong>LAP</strong> button, wich, when pressed, stores the timer values to a set of four 4-bit tri-state registers.
- There are three LEDs:
  - A <strong>POWER</strong> LED, to see if the circuit board has a power supply connected.
  - A <strong>START_STOP</strong> LED, wich is tied to the button with the same name.
  - An <strong>OVERFLOW</strong> LED, wich toggles when the main timer goes over 59.99 seconds.
- 8 7-segment displays: 4 for the timer and 4 for the lap time.
- Resolution of 10ms.
- Adjustable timer for precision calibration.
- 9V barrel input with reverse polarity protection.
- 5V 2-pin header with reverse polarity protection.
- 3 sizes of mounting screws.
- All the various files (Logisim schematic, Multisim schematic, Ultiboard layout) are included, along with the Gerber exports and a Bill of materials.

## Testing and designing steps

The first step was to design the logic circuit in [Logisim Evolution](https://github.com/logisim-evolution/logisim-evolution), for an easy to change desing, while also not having to worry about the various electrcical rules.

![Logisim](https://github.com/AndreiBertescu/TTL_Timer/assets/126001291/94f2c2b7-cd8f-4718-8d29-b4a40fc91957)

<br>The next steps were to draw the electrical schematic and test it. For these steps, the Multisim/Ultiboard duo from National Instruments was used. Multisim, in particular, was chosen over more mainstream programs such as KiCad for its real-time simulation feature, which helped ensure the PCB would work as intended from the first try.

<p align="center">
  <img src="https://github.com/AndreiBertescu/TTL_Timer/assets/126001291/c77c7a58-84b7-4485-b0f5-695524729319" width="400" alt="Image 1">
  <img src="https://github.com/AndreiBertescu/TTL_Timer/assets/126001291/aa5383b3-349a-4b3a-b20f-150717acbd70" width="400" alt="Image 2">
</p>

<br>Next was drawing the layout:
- The PCB is a 19.0 cm x 13.3 cm 2-layer board.
- It has 3mm, 4mm, and 5mm mounting holes intended for standoff screws.
- It has a GND copper plane on both layers.
- All signal traces are 0.254 mm, while the 5V power trace is double the size, at 0.508 mm.
- An additional hole for the power regulator heatsink was added.
- Four additional holes were added to allow replacing the 555 timer potentiometer with two resistors tied in series.
- Proper names were added for the various components, along with description text and a nice drawing.

![image](https://github.com/AndreiBertescu/TTL_Timer/assets/126001291/778a38c2-3f4b-4012-9341-244a571aa682)

The final steps were to order the parts, the PCB, and assemble the board.

- The various components were ordered from [TME](https://www.tme.eu/en/)
- The PCB was ordered from [Jlcpcb](https://jlcpcb.com/)

## Components
- 8 7-segment displays
- 3 LEDs
- 3 10nF ceramic capacitors
- 1 1uF electrolytic capacitor
- 1 1N4002 rectifier diode
- 1 10k trimmer potentiometer
- 3 push switches
- 1 barrel connector
- 2 header pins
- 1 LM7805 power regulator
- 4 4-bit tri-state registers
- 8 4-bit BCD decoders
- 4 4-bit counters
- 2 quad AND gate chips
- 1 quad NOR gate chip
- 1 dual JK flip-flop chip
- Various resistors

## Final statistics
- Total cost:
  - Components: 200 RON
  - PCB: 98 RON
- Total hours of work:
  - Designing schematic and testing: 4 hours
  - Making layout: 6 hours
  - Assembling PCB: 3 hours
 
## Extra photos
![Real1](https://github.com/AndreiBertescu/TTL_Timer/assets/126001291/27111d0e-5ae1-4a51-98e1-2af3a9aaa7f3)
![Real3](https://github.com/AndreiBertescu/TTL_Timer/assets/126001291/48ec11d9-0b28-4eee-b7f5-55829f6a1929)
