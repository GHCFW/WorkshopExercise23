# WorkshopExercise23

<br>

# **Programming Exercises**

## **Exercise 1: Sound a buzzer using Raspberry Pi Pico**
Link to the exercise:
    https://wokwi.com/projects/375088126383940609

* Exercise 1.1: Initialize PWM on Buzzer PIN
```python
buzzer = PWM(Pin(15))
```
* Exercise 1.2: Set Frequency

```python
buzzer.freq(frequency)
```
* Exercise 1.3: Turn Off Buzzer

```python
buzzer.duty_u16(0)
```
Understanding the firmware code:

MicroPython: 

https://github.com/micropython/micropython/blob/0bafdaf5f0f44295597cf2db8c36447675183339/ports/rp2/machine_pwm.c#L274

Raspberry Pi Pico SDK:

https://github.com/raspberrypi/pico-sdk/blob/6a7db34ff63345a7badec79ebea3aaef1712f374/src/rp2_common/hardware_pwm/include/hardware/pwm.h#L274

Data Sheet:

https://datasheets.raspberrypi.com/rp2040/rp2040-datasheet.pdf

## Exercise 2: Control Buzzer with GPIO Input

In this exercise, participants will control the buzzer with a GPIO input using a push button.

* If buzzer is set, playsong. Else turn off the buzzer

```python
button_state = button.value()
if button_state == 1:
    playsong(song)
else:
    bequiet()
```

## Exercise 3: Timer-Based Buzzer Alarm

In this exercise, participants will implement a timer-based buzzer alarm. This section is currently commented out in the code, and participants are encouraged to explore the periodic and one_shot timers.

REFERENCE:
https://docs.micropython.org/en/latest/library/machine.PWM.html?highlight=pwm

<br>


<br>

# Instructions for the Raspberry Pi Pico Board Exercises

## Software Installation

For this level-up lab, we will be using MicroPython to program the Raspberry Pi Pico Firmware. We will use Thonny IDE to program and run the firmware on the board.

### Step 1: Install Thonny
Thonny is a Python based IDE. It supports running MicroPython for Raspberry Pi Pico amongst other micro-controller boards. 

Go to https://thonny.org/ and download the latest version (4.1.2) for your machine.

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

Press the BOOTSEL button and hold it while you connect the other end of the micro-USB cable to your computer. This puts your board into a USB mass storage device mode. You should see the device show up as RP1/RP2 



References:

https://projects.raspberrypi.org/en/projects/getting-started-with-the-pico/2

<br>

# Answer Keys
  * ***Wokwi Exercise*** 
  
   https://wokwi.com/projects/375087692215747585
   
    
<br>
