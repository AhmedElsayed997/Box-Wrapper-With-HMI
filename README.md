# Box-Wrapper-With-HMI

## Project Concept
The goal of this project is to design and implement an automated control system for a machine that
wraps boxes. The system uses two motors:
1. A rotating motor that spins the box.
2. A sliding motor that moves the wrapping unit vertically (up and down) to ensure full coverage of
the box.
The motion is controlled by limit sensors that detect top and bottom positions, a rotation sensor for
counting the number of turns, and timers to control movement frequency and animation.

## System Components
- PLC (Programmable Logic Controller) programmed using CODESYS.
- Two electric motors (one for rotation, one for vertical movement).
- Limit sensors (top and bottom).
- Rotation sensor.
- HMI (Human-Machine Interface) for control and monitoring.
- Software-based counters and timers.

## Implementation Steps
1. Variable Declaration:
 Define control signals, motor outputs, sensor inputs, timers, and counters in the PLC program.
2. PLC Logic (Ladder Diagram):
 Start rotation when the 'START' button is pressed.
 Use a rotation sensor to count the number of box rotations.
 Move the slider up until the upper limit sensor is triggered.
 Then move the slider down until the bottom limit sensor is triggered.
 Timers ('Blinkers') are used to provide visual indicators during movement.
3. HMI Development:
 Display box rotation using the ROTATIO_COUNT_VALUE variable.
 Show slider movement animation using SLIDER_MOVE_ANIMATION.
 Provide START/STOP buttons and display rotation/slider frequencies.
4. Logic-HMI Integration:
 Link all HMI elements to corresponding PLC variables for real-time interaction.
