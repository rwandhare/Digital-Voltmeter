# Digital Voltmeter Circuit

This project demonstrates how to build a simple Digital Voltmeter Circuit using the ICL7107 IC and 555 Timer IC.

## Table of Contents
- [Overview](#overview)
- [Components](#components)
- [Circuit Working](#circuit-working)
- [Key Components Explained](#key-components-explained)
- [How to Build](#how-to-build)
- [License](#license)

## Overview

This project explains the working of a Digital Voltmeter Circuit using the ICL7107 IC, which internally has an integrating converter or dual-type Analog-to-Digital Converter (ADC). The ADC compares the voltage to be measured with an internal reference voltage, converts it into the digital equivalent, and then displays the reading on a seven-segment display.

## Components

1. ICL7107 IC (Analog to Digital Converter)
2. Four Common Anode Seven Segment LED Displays
3. 7805 Voltage Regulator
4. Resistors (1kΩ, 10kΩ, etc.)
5. Capacitors (100nF, 10μF, etc.)
6. 555 Timer IC (for generating negative voltage)
7. Potentiometer (for calibration)
8. Power supply (5V)

## Circuit Working

The internal ADC of the ICL7107 reads the input voltage, compares it with the internal reference voltage, and converts it to a digital value. This digital value is decoded by the internal driver circuit to display the result on four seven-segment LED displays.

1. Clock Generation: Resistor R1 and Capacitor C1 set the internal clock frequency of the ICL7107.
2. Reference Voltage Filtering: Capacitor C2 filters fluctuations in the internal reference voltage, providing a stable reading on the display.
3. Voltage Range Control: Resistor R5 sets the range of the voltmeter. For example, use a 1kΩ resistor for 0-20V range and a 10kΩ resistor for 0-200V range.
4. Calibration: Potentiometer RV1 is used to calibrate the voltmeter by adjusting the reference voltage for the internal ADC.
5. Display: The circuit includes four Common Anode Seven Segment Displays to show the measured voltage and an indicator for negative voltage readings.

The circuit should be powered with a 5V supply, which is regulated by the **7805 voltage regulator IC** to ensure a stable voltage, protecting the ICL7107 from damage.

### Negative Voltage Supply

Pin 26 of the ICL7107 requires a negative power supply, which is generated using the **555 Timer IC** configured as an astable multivibrator. Capacitors 100nF and 10μF are used to achieve the necessary negative voltage. You can modify the capacitor values to optimize the negative voltage output.

## Key Components Explained

1. ICL7107: Handles voltage measurement and drives the seven-segment displays.
2. 7805 Voltage Regulator: Provides stable 5V power supply to the entire circuit.
3. 555 Timer IC: Generates the necessary negative voltage for the ICL7107.
4. Resistor R5: Controls the voltage measurement range (0-20V or 0-200V).
5. Potentiometer RV1: Calibrates the voltmeter to ensure accurate readings.

## How to Build

1. Connect the ICL7107 IC to the seven-segment displays.
2. Use a 555 Timer IC to generate negative voltage.
3. Adjust the clock frequency with R1 and C1, and filter the reference voltage with C2.
4. Set the measurement range with R5 and calibrate the system using RV1.
5. Power the circuit using a 5V supply regulated by the 7805 IC.
6. Assemble the circuit and test it by measuring the voltage of a known source.


## License

This project is open-source and licensed under the MIT License.
