# WorkshopExercise23

<br>

# **Programming Exercises**

## **Exercise 1: Sound a buzzer using Raspberry Pi Pico**
Link to the exercise:
    https://wokwi.com/projects/374763784064202753

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
MicroPython: https://github.com/micropython/micropython/blob/0bafdaf5f0f44295597cf2db8c36447675183339/ports/rp2/machine_pwm.c#L274
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

In this exercise, participants will implement a timer-based buzzer alarm. This section is currently commented out in the code, and participants are encouraged to complete it.

REFERENCE:
https://docs.micropython.org/en/latest/library/machine.PWM.html?highlight=pwm

<br>
