# Reaction Game with Timeout

## Introduction
In this exercise, you will enhance the reaction game code provided to include a timeout feature for each round.

## Exercise Overview
The goal of this exercise is to modify the existing code for the reaction game to include a timeout for each round. 
You will add a timeout mechanism to each round, where if neither player presses a button within a certain time frame, the round ends, and the game announces a timeout.

## Exercise Steps
Follow these steps to complete the exercise:

### Step 1: Configure the Timeout Timer
In this step, you will configure a timer to handle timeouts for each round. The timer will trigger a timeout event if neither player presses a button within a specified time frame.

**EXERCISE 4.1:**

In the `play_round(game_iteration, left_button, right_button)` function configure the timeout timer. Use the `Timer` module to set up the timer.

<code>
timeout_timer = Timer(period=1000, mode=Timer.ONE_SHOT, callback=timeout_callback)
</code>

This code creates a timer that triggers a `timeout_callback` function after 1000 milliseconds (1 second) in one-shot mode. The `timeout_callback` function will handle the timeout event.

### Step 2: Implement the Timeout Callback
In this step, you will implement the `timeout_callback` function, which will be called when the timeout timer expires. This function will end the current round and announce a timeout.

**EXERCISE 4.2:**

Add the `timeout_callback` function. This function sets a global flag `timeout_triggered` to `True` when called.


<code>
def timeout_callback(timer):
    global timeout_triggered
    timeout_triggered = True
</code>


### Step 3: Handle Timeout in the Game Round Logic
Now that you have configured the timer and implemented the timeout callback, you need to modify the game logic to handle timeouts.

**EXERCISE 4.3:**

Within the while loop inside the `play_round` function, add a condition to check if the `timeout_triggered` flag is set to `True`. If it is, print a message indicating a timeout and break out of the loop.

<code>
while True:
    global fastest_button, player2_wins, player1_wins, timeout_triggered
    
    if timeout_triggered:
        print('Game iteration #' + str(game_iteration + 1) + ' resulted in a timeout')
        break
    # ... (existing code)
</code>

### Step 4: Clear `timeout_triggered` Before Each Round
Before each round, it's important to clear the `timeout_triggered` variable to ensure that the timeout state from the previous round does not carry over.

**EXERCISE 4.4:**

In the game loop before calling `play_round()`, add code to set the `timeout_triggered` flag to `False`. This should be done at the beginning of each round.

<code>
timeout_triggered = False
play_round(game_iteration, left_button, right_button)
</code>


## Conclusion
Congratulations! You have successfully added a timeout feature to the reaction game on your Raspberry Pi Pico. This feature adds an extra challenge to the game and ensures that rounds do not go on indefinitely. You can now enjoy playing the enhanced reaction game with your friends or explore further modifications to the code. Happy coding!
