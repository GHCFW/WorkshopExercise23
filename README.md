# The Power of Firmware: Bringing Your Hardware to Life

## Workshop Overview
Welcome to the GHC 2023 The Power of Firmware level-up lab! In this 1-hour session, you will learn key firmware development concepts. You will have the opportunity to practice these concepts using an online simulator called Wokwi as well as real hardware, the Raspberry Pi Pico board.

## Prerequisites
Before getting started, please install the required software needed for this lab as listed here:
[Prerequisites Guide](https://github.com/GHCFW/WorkshopExercise23/blob/main/Prerequisite.md)

## Workshop Contents
### **1. Play the reaction game on Raspberry Pi Pico board <br>**
   **Goal of the game**<br>
   This is a game of quick reflexes! <br>
    &nbsp; &nbsp; * It is a 2-player game, create groups of 2 on your table. <br>
    &nbsp; &nbsp; * The game consists of three rounds where the on-board LED turns on and off as the stimulus. <br>
    &nbsp; &nbsp; * The first player to press their button as soon as the LED goes off wins a point. <br>
    &nbsp; &nbsp; * The player with the most points at the end of three rounds wins the game. <br>
    &nbsp; &nbsp; * The LED has been configured to stay on for an arbitary amount of time. Button presses while the LED is still on will be ignored. <br>

   We have setup the Pico board along with 2 switches for you. The firmware has been flashed on the board. All you need to do for this step is: <br>
     &nbsp; &nbsp; a. Connect the board to your computer <br>
     &nbsp; &nbsp; b. Open Thonny IDE <br>
     &nbsp; &nbsp; c. Connect the board to run with Thonny (check the link below for step by step instructions) <br>
     &nbsp; &nbsp; d. Open and run the code <br>
     &nbsp; &nbsp; e. Play the game!! <br>
     &nbsp; &nbsp; f. Ensure everyone on the table gets a chance to play the game once!! <br>

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

