# UART Menu-Driven Utility for LED and PWM Control

This project demonstrates a menu-driven utility over UART for controlling an LED and a PWM signal using an embedded microcontroller. Through UART commands, users can initiate LED blinking with variable delay and control PWM intensity using a button (PC13). The program offers three main functionalities: LED control with dynamic delay adjustment, PWM intensity control, and exit functionality.

## Features

1. **LED Blinking Control**:
   - Starts an LED blinking sequence.
   - Allows adjustment of the LED blink delay in real-time by pressing a button on PC13.

2. **PWM Intensity Control**:
   - Initiates a PWM signal to control the intensity of an LED.
   - The button (PC13) allows the user to adjust PWM duty cycle, thereby changing LED brightness.

3. **Exit Utility**:
   - Exits the UART utility and stops all ongoing operations.

Users can select options by entering `1`, `2`, or `3` in the UART terminal.

## Requirements

- **Microcontroller**: STM32 or similar, configured to read UART and GPIO inputs.
- **UART Interface**: Configured to handle command input and feedback.
- **Button**: Connected to `PC13` for input.
- **LED**: Connected to a PWM-capable GPIO pin.

## Setup Instructions

1. **Configure UART**:
   - Initialize UART with a baud rate compatible with your terminal (e.g., 9600).
   - Set up an interrupt or polling-based UART receive to handle user input.

2. **Configure GPIO and Button**:
   - Configure `PC13` as a digital input to register button presses.
   - Set up an interrupt on `PC13` to detect rising or falling edges (based on your application).

3. **Configure LED and PWM**:
   - Connect the LED to a PWM-capable GPIO pin.
   - Initialize PWM with a base frequency, adjusting the duty cycle as per user input.

## Code Structure

1. **Main Loop**:
   - Continuously checks UART input for commands.
   - Executes respective functions based on user selection.

2. **LED Blinking Function**:
   - Starts the LED blinking process.
   - Detects button press on `PC13` to adjust blink delay dynamically.

3. **PWM Control Function**:
   - Initializes PWM for LED intensity control.
   - Adjusts duty cycle based on button press to vary brightness.

4. **Exit Function**:
   - Stops all operations and gracefully exits the menu utility.

## Usage

1. Connect to the UART interface using a terminal application (e.g., Tera Term, PuTTY).
2. Enter the desired command (1, 2, or 3) to invoke a specific function:
   - `1`: Starts LED blinking; press the button to change delay.
   - `2`: Starts PWM LED control; press the button to adjust brightness.
   - `3`: Exits the utility.

## Example Commands

- **Start LED Blinking**: Type `1` and press Enter.
- **Adjust LED Blinking Delay**: Press the button (PC13) to cycle through preset delays.
- **Start PWM for LED Intensity**: Type `2` and press Enter.
- **Adjust LED Intensity**: Press the button (PC13) to cycle through brightness levels.
- **Exit Utility**: Type `3` and press Enter.


## Menu Options

Upon connecting to the UART interface, the following menu is displayed:
<p align="center">
    <img src="https://github.com/Sugamshaw/Menu-driven-utility-using-uart-Rx---embedded-c/blob/main/A_PROJECT_2/Picture/a1.png" alt="Menu Option 1" width="256" height="450">
    <img src="https://github.com/Sugamshaw/Menu-driven-utility-using-uart-Rx---embedded-c/blob/main/A_PROJECT_2/Picture/a2.png" alt="Menu Option 2" width="256" height="450">
    <img src="https://github.com/Sugamshaw/Menu-driven-utility-using-uart-Rx---embedded-c/blob/main/A_PROJECT_2/Picture/a3.png" alt="Menu Option 3" width="256" height="450">
    <img src="https://github.com/Sugamshaw/Menu-driven-utility-using-uart-Rx---embedded-c/blob/main/A_PROJECT_2/Picture/a4.png" alt="Exit Option" width="256" height="450">
</p>


## Output

<table>
  <tr>
    <td><img src="https://github.com/Sugamshaw/Menu-driven-utility-using-uart-Rx---embedded-c/blob/main/A_PROJECT_2/Picture/a5.png" alt="Alt text 1" width="256" height="450"></td>
  </tr>
  <tr>
    <td><img src="https://github.com/Sugamshaw/Menu-driven-utility-using-uart-Rx---embedded-c/blob/main/A_PROJECT_2/Picture/a6.png" alt="Alt text 4" width="256" height="450"></td>
  </tr>
  <tr>
    <td><img src="https://github.com/Sugamshaw/Menu-driven-utility-using-uart-Rx---embedded-c/blob/main/A_PROJECT_2/Picture/a7.png" alt="Alt text 7" width="256" height="450"></td>
  </tr>
  <tr>
    <td><img src="https://github.com/Sugamshaw/Menu-driven-utility-using-uart-Rx---embedded-c/blob/main/A_PROJECT_2/Picture/a8.png" alt="Alt text 10" width="256" height="450"></td>
  </tr>
</table>

## Contributing

Feel free to contribute by adding additional features or improving the existing codebase. Please create a pull request with a description of your changes.

---

Happy coding!
