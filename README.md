# VERSION 2.1

Author: Matt Proctor

Creation: 2022-01-13

Version 2.1 removes the need to choose how you resolved the merge conflict. User now presses enter to confirm
that the conflict has been resolved and it will continue.

Version 2.0 automates the cherry-picking commands. No longer outputs to pick.sh, but holds them in an array.
Goes through all commands and executes them. If merge conflict occurs it automatically opens VS code
for the user to solve the merge conflict and then prompts the user for how they resolved it. Based off
of that, it automatically chooses to cherry-pick --abort or cherry-pick --continue and moves on to the
next branch until all branches are cherry-picked

## Setup Help:
1. Save this file in /usr/local/bin so you can call it from anywhere
2. Call this from inside of the repo after you have made the fix
3. VSCode will be opened whenever a merge conflict is encountered
4. Press Enter to continue after you have resolved the conflict
