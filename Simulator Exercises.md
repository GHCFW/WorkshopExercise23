We'll be using Raspberry Pi Pico in MicroPython on [Wokwi](https://wokwi.com) as the tool for the following simulator based exercises. This online simulator provides us a mechanism to verify our code prior to running it on the Silicon.


## **Exercise 1: Let's make some music!**
In this exercise we will create and play a song by programming an external peripheral device "buzzer". We will utilize Raspberry Pi Pico's internal PWM (Pulse Width Modulation) module for our musical creation.
We'll be using three parameters to program our music - frequency, duty cycle and duration (duration each note should play for). We'll utilize APIs from the MicroPython's PWM library for programming the frequency and the duty cycle and the time library for programming the duration for each musical note.

The baseline code for this exercise can be accessed here: [Wokwi Exercise 1](https://wokwi.com/projects/375268852560044033)

* Exercise 1.1: Initialize PWM on Buzzer PIN<br>
    A GPIO pin has already been assigned for the buzzer "BUZZER_PIN".
    - Program that pin as a GPIO OUT pin for the buzzer to generate audio
    - Enable PWM on that pin using PWM() API

```python
buzzer = PWM(Pin(BUZZER_PIN), Pin.OUT)
```


* Exercise 1.2: Set Frequency<br>
    Go to playton() function defined in the exercise.<br>

    This function takes frequency and duration as the input parameters and configures different PWM parameters (frequency, duty cycle and duration).

    Duty_cycle is already configured for you using duty_u16() API from the PWM library. u16 stands for unsigned 16-bits and it defines the resolution for the duty cycle. It can take any value from 0..65535.

    We utilize the sleep_ms() API from utime library to set the duration each note should play for. This acts as a NOP for the CPU and allows the note to be played for the duration specified in milliseconds.

    Use PWM library's frequency API to configure the frequency for the buzzer.

```python
buzzer.freq(frequency)
```
* Exercise 1.3: Turn Off Buzzer
    Go to bequiet() function defined in the exercise.<br>
    The goal of this function is to turn off the buzzer. We can do so by controlling the power to the buzzer via duty cycle. 0 duty cycle means no power is supplied to the buzzer, equivalent of the buzzer being    turned off. 
```python
buzzer.duty_u16(0)
```

To put together all the pieces of this code jump to playsong(mysong) which plays the tones provided in the mysong. Time to run the simulation!


Understanding the firmware code:<br>
&nbsp; [MicroPython PWM API](https://github.com/micropython/micropython/blob/0bafdaf5f0f44295597cf2db8c36447675183339/ports/rp2/machine_pwm.c#L274) <br>
&nbsp; [C SDK PWM API](https://github.com/raspberrypi/pico-sdk/blob/6a7db34ff63345a7badec79ebea3aaef1712f374/src/rp2_common/hardware_pwm/include/hardware/pwm.h#L274) <br>
&nbsp; [Raspberry Pi Pico Data Sheet](https://datasheets.raspberrypi.com/rp2040/rp2040-datasheet.pdf)

[Answer Key for Exercise 1](https://wokwi.com/projects/375268768525056001)

## Exercise 2: Control Buzzer with GPIO Input
In the previous exercise, we learned how to program the different functionality of the PWM module and the buzzer to create music. However, we didn't have the capability to turn it off or on.
In this exercise, participants will control the buzzer with a GPIO input using a slider switch button. If the switch is turned on, play the song, else turn off the buzzer. Else turn off the buzzer
A GPIO pin (IN) has already been defined to take in the input from the switch: SWITCH_PIN. The switch we used has 3 prongs: one end of the switch is connected to 3V, the middle prong is connected to GPIO pin defined by SWITCH_PIN and the other end is connected to GND. We have configured Pico to pull down this pin to ground to avoid any noisy inputs. The switch is considered "ON" when we read a 1 (when the circuit is connected b/w 3V and GPIO pin) and is considered "OFF" when we read a 0 (circuit is connected between the GPIO pin and GND) from the GPIO pin.

Update the while loop that polls to read the switch state. If the switch returns a 1, play the song, else turn off the buzzer <br>

```python
while True:
    switch_state = switch.value()
    if switch_state == 1:
        #print("Switch is ON")
        playsong(song)
    else:
        #print("Switch is OFF")
        bequiet()
```

## Exercise 3: Timer-Based Buzzer Alarm

In this exercise, participants will implement a timer-based buzzer alarm. This section is currently commented out in the code, and participants are encouraged to explore the periodic and one_shot timers.
This exercise utilizes interrupts to generate an event for the CPU when the timer period has elapsed to play the song.

REFERENCES:<br>
[Wokwi Switch Documentation](https://docs.wokwi.com/parts/wokwi-slide-switch)
[Wokwi Buzzer Documentation](https://docs.wokwi.com/parts/wokwi-buzzer)
[MicroPython PWM Documentation](https://docs.micropython.org/en/latest/library/machine.PWM.html?highlight=pwm)
<br>

# Answer Key <br>
[Simulator Exercises Answer Key](https://wokwi.com/projects/375268338959054849)

