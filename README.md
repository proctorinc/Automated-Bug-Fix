# VERSION 1.0

Author: Matt Proctor

Creation: 2021-01-06

Version 1.0 automates the creation of the cherry-picking commands by taking the git repo that it is called in
and collecting the branches. It then removes unwanted branches, adds in checkout commands and 
cherry-pick commands with the commit id and saves them all into pick.sh, which can be saved wherever 
the user prefers. User runs pick.sh, solves merge conflicts and manually removes previously cherry-picked
branches until everything is solved.

## Setup Help:
1. Save this file in /usr/local/bin so you can call it from anywhere
2. Change output location (below) to where you want to save the output pick.sh file
	(preferably in the folder where your repos are)
3. Once you make the fix, stay in the repo and call this script, pick.sh will be created in your
	designated output location and you can continue cherrypicking normally
