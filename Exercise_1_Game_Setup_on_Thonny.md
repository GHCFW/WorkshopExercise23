## Exercise 1: Play the reaction game on the Pico board

   **Goal of the game**<br>
    The game consists of three rounds where an LED turns on and off as the stimulus. The objective for each player is to press their respective button as quickly as possible when the LED turns on->off.
    The player who reacts fastest in each round earns a point, and the player with the most points at the end of three rounds wins the game.

   We have setup the Pico board along with 2 switches for you. The micropython firmware as well as the game firmware has been flashed on the board.
   
   1. Verify bread-board setup <br>
      Check the picture below to verify your bread-board setup matches the expectation. <br>

      ![Exercise_1_Breadboard_Setup](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Exercise_1_Breadboard_Setup.jpg)

      The button we are using has 2 prongs, one end of the switch is connected to Pico's GPIO pin and the other end is connected to 3V rail.
      - Player 1 button connections: GPIO Pin "TODO", which is equivalent to bread-board pin "TODO".
      - Player 2 button connections: GPIO Pin "TODO", which is equivalent to bread-board pin "TODO".

      Pico's 3V is GPIO Pin "TODO", which is equivalent to bread-board pin "TODO".

  You can refer to the [Raspberry Pi Pico pinout diagram](https://datasheets.raspberrypi.com/pico/Pico-R3-A4-Pinout.pdf?_gl=1*1ish86u*_ga*MTc0NDY1MTcyMC4xNjk0MDQ3NTcw*_ga_22FD70LWDS*MTY5NDA1MTUwNC4yLjAuMTY5NDA1MTUwNS4wLjAuMA..) for this lab.


  3. Connect the board to your computer <br>
     Use the USB/USB converter to connect the board to your computer.
     The host computer supplies power to the board, but also provides a mechanism to run the firmware.

  4. Open Thonny & Connect the board to run with Thonny <br>
     3a. Close the window. Go back to the three horizontal lines icon and select "MicroPython (Raspberry Pi Pico) @ [drive that the board is mounted on]."

       - Example: "MicroPython (Raspberry Pi Pico) Board CDC @ COM3" (OR) "MicroPython (Raspberry Pi Pico) Board in FS Mode @ /dev/..."
       - This shows that the board is connected to a specific port (e.g., COM3), but the port number may vary depending on your computer.

        ![MicroPython COM Port](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/MicroPython_COM.jpg)

  3b. Verify that the shell has been updated to the MicroPython version you selected, and it shows "Raspberry Pi Pico with RP2020."

   ![RP2040 Shell](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/rp2040_shell.jpg)

  You are all set to run MicroPython code on your board!
  
  4. Play the game!! <br>
