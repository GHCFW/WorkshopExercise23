## The Power of Firmware - Bringing Your Hardware to Life Workshop

Welcome to "The Power of Firmware - Bringing Your Hardware to Life" workshop! In this workshop, you'll learn firmware concepts used regularly and materialize them by creating a simple and fun game that determines the fastest button press between two players using a Raspberry Pi Pico board.

### Prerequisites

Before you start, make sure you have completed the following prerequisites:

- [Install Thonny](https://github.com/GHCFW/WorkshopExercise23/blob/main/Prerequisite.md): Thonny is a Python IDE that we'll use to program the Raspberry Pi Pico. It's essential for this workshop.

### Getting Started with Wokwi

1. **Wokwi Simulation**: We'll start by simulating the game on the Wokwi platform. Follow this link to open the simulation: [Wokwi Simulation](https://wokwi.com/projects/375362750523243521).

2. **Understanding the Code**: Take a look at the provided Python code in `main.py`. We've added comments to explain the code step by step. It includes concepts like GPIO (General-Purpose Input/Output) pins and interrupts which we discussed earlier

3. **Running the Simulation**: On the Wokwi platform, you can't truly play the game because you can't press both buttons at once. However, you can observe how the code works by clicking the "Start Simulation" button.

4. **Exploring Concepts**: While in the simulation, explore how GPIO pins are used to read button presses and how interrupts are triggered when a button is pressed. This will be essential when you move to the hardware board.

### Moving to the Hardware Board

Now that you've familiarized yourself with the code and concepts, it's time to move to the Raspberry Pi Pico hardware board.

#### Step 2: Configure Thonny to run MicroPython for Raspberry Pi Pico

1. Click on the three horizontal lines icon in the bottom right corner of the Thonny IDE.

   ![Configure Interpreter](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Thonny_Configure_Interpreter.png)

2. Select "Configure Interpreter."

3. In the dialog that appears, choose "MicroPython for Raspberry Pi Pico" as the interpreter. Keep the remaining options as default.

   ![MicroPython Configuration](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Thonny_MicroPython.jpg)

   Note: You may see this option only when the board is connected to your computer. We'll connect the board in the next step.

#### Step 3: Add MicroPython Firmware to the Raspberry Pi Pico Board

1. To install MicroPython firmware on your Raspberry Pi Pico board, first, locate the BOOTSEL button on the board.

   ![BOOTSEL Button](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/BOOTSEL.jpg)

2. Press and hold the BOOTSEL button while connecting the other end of the micro-USB cable to your computer. This action puts your board into USB mass storage device mode, and it should appear as "RP1-RP2."

   ![RP1-RP2](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/RP1_RP2.jpg)

   Note: If you don't see the device show up, disconnect the board, hold down the BOOTSEL button, and then connect it to the computer while continuing to hold the button.

3. Open Thonny and select "Install MicroPython" from the three horizontal lines icon.

   ![Install MicroPython](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Install_MicroPython.jpg)

4. Make sure to select the following options:
   - Target volume: RP1-RP2 (D:) (The drive name may be different for you)
   - MicroPython Family: RP2
   - Variant: Raspberry Pi Pico/Pico H
   - Version: 1.20.0

   ![MicroPython Installation Details](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Install_MicroPython_Details.jpg)

5. Click "Install." Once it's done, you should see "Done!" in the bottom-left window.

   ![Installation Done](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/MicroPython_Install_Done.jpg)

6. Close the window. Go back to the three horizontal lines icon and select "MicroPython (Raspberry Pi Pico) @ [drive that the board is mounted on]."

   - Example: "MicroPython (Raspberry Pi Pico) Board CDC @ COM3" (OR) "MicroPython (Raspberry Pi Pico) Board in FS Mode @ /dev/..."
   - This shows that the board is connected to a specific port (e.g., COM3), but the port number may vary depending on your computer.

   ![MicroPython COM Port](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/MicroPython_COM.jpg)

7. Verify that the shell has been updated to the MicroPython version you selected, and it shows "Raspberry Pi Pico with RP2020."

   ![RP2040 Shell](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/rp2040_shell.jpg)

You are all set to run MicroPython code on your board!

#### Step 4: Run MicroPython Code on Raspberry Pi Pico Board

Once you have tested your code on a simulator and you are ready to deploy it on the Raspberry Pi Pico, follow these steps:

1. Copy your code over to the Thonny IDE. Note: You can also develop code directly in Thonny. But let us copy over what we have in Wokwi in the interest of time. 

2. Select "Save As," give your file a name, and choose "Save to Raspberry Pi Pico board". Since the board is in BOOTSEL mode this will save the file on your board.

   ![Save Code to Raspberry Pi Pico](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/save_code_on_rp.jpg)

3. Connect all external peripherals to the board using connecting wires or a breadboard.

   - We have already connected them for you in the interest of time. But please refer to your board's pinout diagram to ensure that the GPIO pins you use to connect the peripherals match the code's expectations.

   - You can refer to the [Raspberry Pi Pico pinout diagram](https://datasheets.raspberrypi.com/pico/Pico-R3-A4-Pinout.pdf?_gl=1*1ish86u*_ga*MTc0NDY1MTcyMC4xNjk0MDQ3NTcw*_ga_22FD70LWDS*MTY5NDA1MTUwNC4yLjAuMTY5NDA1MTUwNS4wLjAuMA..) for this lab.

Now you are ready to hit "Play." Click the "Run" button to execute your code on the board.

Any debug statements or errors you encounter that you added to your code will show up in the Python shell.

References:
- [Raspberry Pi Pico Workshop](https://projects.raspberrypi.org/en/projects/getting-started-with-the-pico/2)

