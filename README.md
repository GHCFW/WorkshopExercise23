# The Power of Firmware: Bringing Your Hardware to Life

## Workshop Overview
Welcome to the GHC 2023 The Power of Firmware level-up lab! In this 1-hour session, you will learn key firmware development concepts. You will have the opportunity to practice these concepts using an online simulator called Wokwi as well as real hardware, the Raspberry Pi Pico board.

## Prerequisites
Before getting started, please install the required software needed for this lab as listed here:
[Prerequisites Guide](https://github.com/GHCFW/WorkshopExercise23/blob/main/Prerequisite.md)

## Workshop Contents
### **1. Play the reaction game on Raspberry Pi Pico board <br>**
   **Goal of the game**<br>
    The game consists of three rounds where an LED turns on and off as the stimulus. The objective for each player is to press their respective button as quickly as possible when the LED turns on->off.
    The player who reacts fastest in each round earns a point, and the player with the most points at the end of three rounds wins the game.

   We have setup the Pico board along with 2 switches for you. The firmware has been flashed on the board. All you need to do for this step is:
   
   a. Connect the board to your computer <br>
   b. Open Thonny IDE <br>
   c. Connect the board to run with Thonny (check the link below for step by step instructions) <br>
   d. Run the code <br>
   e. Play the game!! <br>

   Visit [Exercise 1: Game Setup on Thonny](https://github.com/GHCFW/WorkshopExercise23/blob/main/Exercise_1_Game_Setup_on_Thonny.md) for detailed instructions
   
### **2. Update the reaction game to play victory music on the simulator <br>**
   We will start with this exercise on the simulator (Wokwi) before trying the code on the board. <br>
   **Goal** <br>
   You have been provided with a song library with song options: 'player1_victory_song', 'player2_victory_song'. <br>
   Update the existing code to play the corresponding victory tone when a player wins the round. <br>

   Visit [Exercise 2: Play victory song on Wokwi](https://github.com/GHCFW/WorkshopExercise23/blob/main/Exercise_2_Play_Victory_Song_on_Wokwi.md) for detailed instructions

### **3. Play the reaction game with the buzzer on the Pico board <br>**
   **Goal** <br>
   The goal of this exercise is to play the same victory music on the board!

   a. Connect the buzzer to the board (check the link below for instructions) <br>
   b. Copy the code from Wokwi to Thonny IDE (keep the same file names, save the files on the Raspberry Pi Pico Board) <br>
   c. Play the game! <br>

   Visit [Exercise 3: Play victory song on Board](https://github.com/GHCFW/WorkshopExercise23/blob/main/Exercise_3_Play_Victory_Song_on_Board.md) for detailed instructions


## Troubleshooting

## Resources

* You bought a new Pico board. What next? See setup instructions for a new board here <>, project ideas here <>

