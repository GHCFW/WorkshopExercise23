We'll be using Raspberry Pi Pico in MicroPython on [Wokwi](https://wokwi.com) as the tool for the following simulator based exercises. This online simulator provides us a mechanism to verify our code prior to running it on the Silicon.


## **Exercise 1: Let's make some music!**
In this exercise we will create and play a song by programming an external peripheral device "buzzer". We will utilize Raspberry Pi Pico's internal PWM (Pulse Width Modulation) module for our musical creation.
We'll be using three parameters to program our music - frequency, duty cycle and duration (duration each note should play for). We'll utilize APIs from the MicroPython's PWM library for programming the frequency and the duty cycle and the time library for programming the duration for each musical note.

The baseline code for this exercise can be accessed here: [Wokwi Exercise](https://wokwi.com/projects/375088126383940609)

* Exercise 1.1: Initialize PWM on Buzzer PIN<br>
 Let's start by initializing the GPIO pin the buzzer is connected to as a PWM pin.

```python
buzzer = PWM(Pin(15))
```

* Exercise 1.2: Set Frequency<br>
Utilize the PWM's freq API to the set frequency of the musical note to play.

```python
buzzer.freq(frequency)
```
* Exercise 1.3: Turn Off Buzzer<br>
Duty cycle of 0 means no power is supplied to the buzzer. Let's use that capability to turn off the buzzer.

```python
buzzer.duty_u16(0)
```

If you now hit play in your simulation, you should be able to hear the music!

Understanding the firmware code:<br>
&nbsp; [MicroPython PWM API](https://github.com/micropython/micropython/blob/0bafdaf5f0f44295597cf2db8c36447675183339/ports/rp2/machine_pwm.c#L274) <br>
&nbsp; [C SDK PWM API](https://github.com/raspberrypi/pico-sdk/blob/6a7db34ff63345a7badec79ebea3aaef1712f374/src/rp2_common/hardware_pwm/include/hardware/pwm.h#L274) <br>
&nbsp; [Raspberry Pi Pico Data Sheet](https://datasheets.raspberrypi.com/rp2040/rp2040-datasheet.pdf)


## Exercise 2: Control Buzzer with GPIO Input
In the previous exercise, we learned how to program the different functionality of the PWM module and the buzzer to create music. However, we didn't have the capability to turn it off or on.
In this exercise, participants will control the buzzer with a GPIO input using a slider button.

* If the button is turned on, let's play the song. Else, turn off the buzzer.

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
[MicroPython PWM Documentation](https://docs.micropython.org/en/latest/library/machine.PWM.html?highlight=pwm)

<br>
