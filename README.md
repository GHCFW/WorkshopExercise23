# WorkshopExercise23

<br>

# **Programming Exercises**

## **Exercise 1: Sound a buzzer using Raspberry Pi Pico**
Go to [Exercise](https://wokwi.com/projects/375088126383940609)

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

[MicroPython PWM API](https://github.com/micropython/micropython/blob/0bafdaf5f0f44295597cf2db8c36447675183339/ports/rp2/machine_pwm.c#L274)

[C SDK PWM API](https://github.com/raspberrypi/pico-sdk/blob/6a7db34ff63345a7badec79ebea3aaef1712f374/src/rp2_common/hardware_pwm/include/hardware/pwm.h#L274)

[Raspberry Pi Pico Data Sheet](https://datasheets.raspberrypi.com/rp2040/rp2040-datasheet.pdf)

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
[MicroPython PWM Documentation](https://docs.micropython.org/en/latest/library/machine.PWM.html?highlight=pwm)

<br>

# Instructions for programming the Raspberry Pi Pico Board
[Programming the Pi Pico Board](https://github.com/GHCFW/WorkshopExercise23/blob/main/Instructions%20for%20RP%20Pi%20Board%20Setup.md)

# Further Reading/References
## Raspberry Pi Pico

[Getting Started with Raspberry Pi Pico](https://www.raspberrypi.com/documentation//microcontrollers/)

[Raspberry Pi Pico Data Sheet](https://datasheets.raspberrypi.com/rp2040/rp2040-datasheet.pdf)

[Raspberry Pi Pico MicroPython SDK](https://datasheets.raspberrypi.com/pico/raspberry-pi-pico-python-sdk.pdf)

[Raspberry Pi Pico Pico C/C++ SDK](https://datasheets.raspberrypi.com/pico/raspberry-pi-pico-c-sdk.pdf)

[Pico MicroPython Examples](https://github.com/raspberrypi/pico-micropython-examples)

[Pico Examples](https://github.com/raspberrypi/pico-examples)

[RP2040 Datasheet](https://datasheets.raspberrypi.com/rp2040/rp2040-datasheet.pdf)

[Raspberry Pi Pico Pinout](https://datasheets.raspberrypi.com/pico/Pico-R3-A4-Pinout.pdf)

## WOKWI
[Wokwi Docs](https://docs.wokwi.com/)

## PWM
[PWM](https://en.wikipedia.org/wiki/Pulse-width_modulation)

## Interrupts
[Interrupt Handler](https://en.wikipedia.org/wiki/Interrupt_handler)

# Answer Key
[Wokwi Exercises Answer Key](https://wokwi.com/projects/375087692215747585)
   
    
<br>
