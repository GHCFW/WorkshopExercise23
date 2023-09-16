## Exercise 3: Play the victory song using a buzzer on the Pico Board


### 1. Let's start by connecting the buzzer to the board. <br>
   Locate the buzzer and some jumper cables (socket-pin style cables) on your table. <br>

  &nbsp; &nbsp; ![Exercise 3: Buzzer](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Buzzer_Connections.jpeg)

  Connect the socket end of the cables to the two pins of the buzzer, and the pin ends of the jumper cables to the bread-board.

  We want to connect the buzzer to the board via: <br>
   &nbsp; &nbsp;- GND, which is connected on the bread-board via 3[abcde] <br>
   &nbsp; &nbsp;- GPIO pin 14, which is connected on the bread-board via 19 [abcde] <br>

   &nbsp; &nbsp; ![Exercise 3: Connecting Buzzer to the Board](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Buzzer_On_Board.jpeg)

   Reference <br>
      [Raspberry Pi Pico pinout diagram](https://datasheets.raspberrypi.com/pico/Pico-R3-A4-Pinout.pdf?_gl=1*1ish86u*_ga*MTc0NDY1MTcyMC4xNjk0MDQ3NTcw*_ga_22FD70LWDS*MTY5NDA1MTUwNC4yLjAuMTY5NDA1MTUwNS4wLjAuMA..)

### 2. Configure Thonny to run the updated firmware for buzzer
  Copy over the code from Wokwi to Thonny.
  - Create a new file on Raspberry Pi Pico, "song.py"
    - Copy the code from Wokwi song.py to here
    - Save the file on Raspbery Pi Pico board
      
  - Create a new file on Raspberry Pi Pico, "tones.py"
    - Copy the code from Wokwi tones.py to here
    - Save the file on Raspbery Pi Pico board

  - Create a new file on Raspberry Pi Pico, "main.py"
    - Copy the code from Wokwi main.py to here
    - Save the file on Raspbery Pi Pico board         

### 3. Play the game!
  Hit run while having "main.py" open. You should see the shell updated with the game running!!
