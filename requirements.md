# Requirements

This project is an Arduino hardware prototype. The requirements are hardware components and Arduino libraries, not Python packages.

## Hardware Components

- Arduino Uno boards, 2 to 3 depending on power stability
- 28BYJ-48 stepper motors, up to 4 depending on the prototype version
- ULN2003 stepper motor driver boards, one per stepper motor
- 3D-printed rails for the dispensing mechanism
- 4 x 4 Arduino keypad
- I2C LCD module, 16 x 2
- Three-pin buttons for the first prototype version
- Breadboards
- Jumper wires / Dupont wires
- Cardboard or other material for the prototype enclosure

## Arduino Libraries

Install these libraries in the Arduino IDE Library Manager:

- Stepper
- Wire
- LiquidCrystal_I2C
- Keypad

In the Arduino IDE, open the Library Manager through:

```text
Sketch -> Include Library -> Manage Libraries
```

You can also open the Serial Monitor with:

```text
Ctrl + Shift + M
```

## Build Notes

- Check the motor pin order carefully. The 28BYJ-48 motor direction depends on the pin sequence used in the `Stepper` constructor.
- The I2C LCD address is commonly `0x27`, but some modules may use a different address.
- The motor loop count was calibrated for the original prototype rail length(3d printed rail bought online). Recalibrate it if the rail size changes.
- Use stable external power if the motors behave inconsistently.
- Test each subsystem separately before combining the motors, keypad, LCD, and enclosure.
