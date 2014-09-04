# Steps to reproduce this problem: #

1. Open a new terminal and resize it to 89x19

2. Open a new tmux session in this terminal:
 
    ```
    tmux new -s epic5-bug
    ```

3. Run epic5 within the tmux session, and fill the output with data:

    ```
    /load dummy-output.irc
    ```

4. Make a note of the last visible output line on screen

5. Open new terminal and resize it to 58x27

6. attach to the previously created tmux session by running the command:

    ```
    tmux attach-session -d -t epic5-bug
    ```

7. Notice the last visible output line on screen, it is different than in step 4
