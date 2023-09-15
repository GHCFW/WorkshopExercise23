## Exercise 1: Play the reaction game on the Pico board

   **Goal of the game**<br>
    The game consists of three rounds where an LED turns on and off as the stimulus. The objective for each player is to press their respective button as quickly as possible when the LED turns on->off.
    The player who reacts fastest in each round earns a point, and the player with the most points at the end of three rounds wins the game.

   We have setup the Pico board along with 2 switches for you. The micropython firmware as well as the game firmware has been flashed on the board.
   
   1. Verify bread-board setup <br>
      Check the picture below to verify your bread-board setup matches the expectation. <br>

      ![Exercise 1: Board Setup](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Exercise_1_Board_Setup.jpeg)

      The button we are using has 2 pins, one end of which is connected to Pico's GPIO pin and the other end is connected to a 3V rail.
      - Player 1 (blue button) button connections: GPIO Pin 15, which is connected to the bread-board via #20 [abcde]
      - Player 2 (white button) button connections: GPIO Pin 16, which is connected to the bread-board via #20 [fghij]

      Pico's 3V is GPIO Pin 36, which is connected to the bread-board via 5 [fghij] to the bread-board's +rails

      Reference <br>
      [Raspberry Pi Pico pinout diagram](https://datasheets.raspberrypi.com/pico/Pico-R3-A4-Pinout.pdf?_gl=1*1ish86u*_ga*MTc0NDY1MTcyMC4xNjk0MDQ3NTcw*_ga_22FD70LWDS*MTY5NDA1MTUwNC4yLjAuMTY5NDA1MTUwNS4wLjAuMA..)


  2. Connect the board to your computer <br>
     Use the USB cable to connect the board to your computer. <br>
     The host computer supplies power to the board, but it also provides a mechanism to run the firmware.

  3. Open Thonny & connect the board to run with Thonny <br>
  
     3a. By default Thonny will open a Python shell, such as like the one shown in the picture below.
     
        ![Thonny Python Shell](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Thonny_Python_Shell.png)

     
     3b. We want to switch the shell to run with MicroPython instead of Python. Locate the three horizontal lines icon in the bottom right window of Thonny. Click and select "MicroPython (Raspberry Pi Pico) @ [drive that the board is mounted on]."

       - Example: "MicroPython (Raspberry Pi Pico) Board CDC @ COM3" (OR) "MicroPython (Raspberry Pi Pico) Board in FS Mode @ /dev/..."
       - This shows that the board is connected to a specific port (e.g., COM3), but the port number may vary depending on your computer.

        ![Pico COM Port on Windows](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/MicroPython_COM.jpg)

        ![TODO: Pico COM Port on Mac](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/MicroPython_COM.jpg)


  3b. Verify that the shell has been updated to the MicroPython version you selected, and it shows "Raspberry Pi Pico with RP2020."

   ![RP2040 Shell](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/rp2040_shell.jpg)

  You are all set to run MicroPython code on your board!
  
  4. Open the firmware code uploaded on Thonny <br>
     Before we can play the game, open the firmware files that are already uploaded on Thonny so that we can run that firmware. To do this, go to File -> Open ... ->

     If you didn't see Raspberry Pi Pico as an option to open the file from:
     - Your board is not recognized by Thonny. Go back to steps 2 & 3 and ensure that those were successful 

  6. Play the game!! <br>
