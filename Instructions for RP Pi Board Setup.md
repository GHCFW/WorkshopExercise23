# Instructions for the Raspberry Pi Pico Board Exercises

## Software Installation

For this level-up lab, we will be using MicroPython to program the Raspberry Pi Pico Firmware. We will use Thonny IDE to program and run the firmware on the board.

### Step 1: Install Thonny
Thonny is a Python based IDE. It supports running MicroPython for Raspberry Pi Pico amongst other micro-controller boards. 

Go to [Thonny](https://thonny.org/) and download the latest version (4.1.2) for your machine.

![alt text](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Thonny_Download.jpg)

Go through the installation wizard to install Thonny. As a part of the IDE installation, it installs its own version of python (In September 2023 it installed Python 3.10). Once installed, launch Thonny.  It should look something like this:

![alt text](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Thonny_Home.jpg)


If you don't see Thonny's Python version in the bottom right window, click on the 3 horizontal lines icon and select Thonny's Python as the interpreter.
You can use the shell to run standard Python code.

### Step 2: Configure Thonny to run MicroPython for Raspberry Pi Pico
Click on the three horizontal lines icon in the bottom right corner of the Thonny IDE, click on Configure Interpreter 

![alt text](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Thonny_Configure_Interpreter.png)

Select MicroPython for Raspberry Pi Pico. Keep the remaining options the same as default.

![alt text](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Thonny_MicroPython.jpg)

Sometimes, you may only see this option when the board is plugged in to the computer. We'll get to connecting the board to the computer next!

### Step 3: Add MicroPython Firmware to the Raspberry Pi Pico Board
As a part of the board setup, we will now install MicroPython firmware on the board. To do that, we will configure Raspberry Pi Pico board as a USB Mass Storage Device. To do that, let's first find the BOOTSEL button on the board.

![alt text](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/BOOTSEL.jpg)

Press the BOOTSEL button and hold it while you connect the other end of the micro-USB cable to your computer. This puts your board into a USB mass storage device mode. You should see the device show up as RP1-RP2 

![alt text](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/RP1_RP2.jpg)

Now let's open Thonny and install MicroPython to our board. Click on the three horizontal lines icon and select install MicroPython from the list.

![alt text](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Install_MicroPython.jpg)

Make sure to select the following options: 

Target volume: RP1-RP2 (D:) (Note the drive name maybe different for you)
MicroPython Family: RP2
variant: Raspberry Pi Pico/Pico H
version: 1.20.0 

![alt text](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Install_MicroPython_Details.jpg)

And hit install. Once it is done you should see Done! in the bottom left window

![alt text](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/MicroPython_Install_Done.jpg)

Close the window. Go back to our favorite 3 horizontal lines icon and select "MicroPython (Raspberry Pi Pico) Board CDC @ COM3"
This shows that the board is connected to COM3 port. The port number may vary depending on your computer.

![alt text](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/MicroPython_COM.jpg)

Make sure the shell has been updated to MicroPython version you selected and shows Raspberry Pi Pico with RP2020.

![alt text](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/rp2040_shell.jpg)

You are all set to run MicroPython code on your board!!

#### Step 4: Run MicroPython Code on Raspberry Pi Pico Board

Once you have tested your code on a simulator and you are ready to deploy it on the Si, let's copy over the code to the Thonny IDE. You can also develop code directly on Thonny. 
Select save as, give a file name and select save to Raspberry Pi Pico board

![alt text](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/save_code_on_rp.jpg)

Attach any external peripherals that you are programming to the board using connecting wires or a breadboard. 

Refer to your board's pinout diagram to ensure the GPIO pins you use to connect the peripherals match the code's expectations. 

Refer to [Raspberrry Pi Pico pinout diagram](https://datasheets.raspberrypi.com/pico/Pico-R3-A4-Pinout.pdf?_gl=1*1ish86u*_ga*MTc0NDY1MTcyMC4xNjk0MDQ3NTcw*_ga_22FD70LWDS*MTY5NDA1MTUwNC4yLjAuMTY5NDA1MTUwNS4wLjAuMA..) for this lab.



Now you are ready to hit play. Select the run button to run your code on the board as shown below: 

![alt text](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/run_the_code.jpg)

Any debug statements or errors you encounter you added will show up in the Python shell. 


References:

https://projects.raspberrypi.org/en/projects/getting-started-with-the-pico/2
