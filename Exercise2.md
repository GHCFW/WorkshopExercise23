# Exercise 2: Adding Sound Effects with PWM

In this exercise, you will enhance your Raspberry Pi Pico game by adding sound effects when a player wins. We'll use PWM (Pulse-Width Modulation) to play musical notes on a buzzer to announce the winner.

## Prerequisites

Before you start this exercise, make sure you have completed [Exercise 1](https://github.com/GHCFW/WorkshopExercise23/blob/main/Exercise1.md), where you learned how to set up your Raspberry Pi Pico and create a game that determines the fastest button press between two players.

## Getting Started

### Step 1: Understanding the Code

To get started, let's understand the code and make the necessary modifications. Click on the following link to open your project in the Wokwi simulator: [Wokwi Simulator - Exercise 2](https://wokwi.com/projects/375439773149315073).

Once the simulator is open, you can explore the code files:

- `main.py`: The main script for the game, which includes code for button handling and determining the winner. This should be familiar since it is built on top of Exercise 1 code.
- `tones.py`: A dictionary of musical note frequencies that we'll use for playing the buzzer.
- `song.py`: Contains functions for playing songs and sound effects.

### Step 2: Configure the Buzzer

You will use a buzzer to play musical notes. Before you can use it, you need to initialize the PWM object for the buzzer.

**FILL ME:**
In the `song.py` file, replace the comment that says `# Exercise 2.1: Init the buzzer pin` with code to initialize the GPIO pin that the buzzer is connected to in GPIO out mode. In other words, what should `buzzer_pin` be set to? 

```python
# Exercise 2.1: Init the buzzer pin
buzzer = machine.PWM(buzzer_pin)

## Step 3: Adding Sound Effects

Now, let's add sound effects to announce the winner. In the `main.py` file, you will find a section where the winner is determined. Your task is to add function calls to play sound effects for the players.

Here's what you need to do:

- When **player 1** wins, add a function call to `playsong()` with whichever song you choose to play for player 1 victory from the options provided in song.py.
- When **player 2** wins, add a function call to `playsong()` for player 2 vicotry song.

## Step 4: Testing on Wokwi

Before porting your code to the Raspberry Pi Pico, it's a good practice to test it quickly on the Wokwi simulator. This allows you to verify that your code is functioning as expected without the need for physical hardware.

To do this, make sure you have made the changes mentioned above in Steps 2 and 3 and test your game in the simulator to ensure that the sound effects work correctly.

## Step 5: Porting to Raspberry Pi Pico

Once you have confirmed that your code works in the Wokwi simulator, you can proceed to port it to your Raspberry Pi Pico using Thonny. Follow the same steps you learned in Exercise 1 to set up Thonny and configure your board.

## Wiring Diagram

Connect the buzzer to the Raspberry Pi Pico as shown in the following diagram:

![Wiring Diagram](diagram.json)

This diagram illustrates the connections between the Raspberry Pi Pico, buttons, LED, and buzzer.

## Additional Resources

- [Raspberry Pi Pico Pinout Diagram](https://datasheets.raspberrypi.com/pico/Pico-R3-A4-Pinout.pdf?_gl=1*1ish86u*_ga*MTc0NDY1MTcyMC4xNjk0MDQ3NTcw*_ga_22FD70LWDS*MTY5NDA1MTUwNC4yLjAuMTY5NDA1MTUwNS4wLjAuMA..)

That's it! You've added sound effects to your Raspberry Pi Pico game using PWM. Have fun playing your improved game!
