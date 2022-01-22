# VERSION 3.2

Author: Matt Proctor

Creation: 2022-01-19

## Contact:
If any issues or edge cases occur that should be handled, please email mproctor@securecodewarrior.com

(For SCW Team Members: slack me on the securecodewarrior slack channel and I will look into fixes and updates)

## About:
Walks you through the process of bug fixing step by step. Automates as many steps as possible.
Automatically determines if repo is a full app and auto creates cherry-picking commands.
Automates cherry-picking process and shows progress. Opens VS code whenever a merge conflict
occurs. Opens up Jira with JQL query in browser with just the CHLC input. Reminds of final
steps for closing, linking, and transitioning all CHLRQ's and CHLC's

## Details:
- Supports minified and full apps, cherry-picks accordingly

- Stops user if errors occur. Ex: not a repo, no changes in repo, invalid input

- Yellow text informs user of manual tasks to perform outside of the program (in browser)

- Gray text with white colon informs user to input information

## Setup and usage help:
1. Save this file in /usr/local/bin so it can be called anywhere:

	command: sudo mv bug-fix-auto /usr/local/bin/bug-fix-auto

	command: sudo chmod +x /usr/local/bin/bug-fix-auto

2. Clone repo from github and have the CMS and Jira tickets open
3. Run the program (-d for debug, -p for nopush for testing):

	command: bug-fix-auto [-d] [-p]

4. Follow the Steps of the program

	- Yellow means manual tasks outside of the program (ie: Jira)

	- White colon means enter data

	- Press [Enter] to confirm steps when prompted

## Version History
Version 3.2 Combined bug-fix-auto and cherrypick officially into one single program.
	Cherrypick is now a method inside of the larger bug-fix program. Added arguments
	for enabling debug mode and nopush mode (doesn't let the program push to the repo
	for testing purposes). Also auto checks for full app and only cherry-picks if it
	is a full app and not minified. Added more user friendly reminders, colored text
	to help users understand functionality.

Version 3.1 added bug-fix-auto program side by side with cherrypick. Runs through bug-fix
	process and calls cherry-pick script when needed. Now encompasses the entire
	bug-fix process. Added in helpful user reminders to do all steps in the process
	and automates as much as it can.

Version 3.0 differs from 2.0 as it automates more of the bug fixing process, including:
        Automatically running jira jql query to avoid manual copying and pasting.

Version 2.1 removes the need to choose how you resolved the merge conflict. User now
	presses enter to confirm that the conflict has been resolved and it will continue.

Version 2.0 automates the cherry-picking commands. No longer outputs to pick.sh, but holds
	them in an array. Goes through all commands and executes them. If merge conflict
	occurs it automatically opens VS code for the user to solve the merge conflict and
	then prompts the user for how they resolved it. Based off of that, it automatically
	chooses to cherry-pick --abort or cherry-pick --continue and moves on to the next
	branch until all branches are cherry-picked
	
Version 1.0 automates the creation of the cherry-picking commands by taking the git repo
	that it is called in and collecting the branches. It then removes unwanted branches,
	adds in checkout commands and cherry-pick commands with the commit id and saves them
	all into pick.sh, which can be saved wherever the user prefers. User runs pick.sh,
	solves merge conflicts and manually removes previously cherry-picked branches until
	everything is solved.

## In progress
1. Validation for Jira CHLC #, if incorrect there is no way to go back

(Work around: use auto-jql program)

2. Possible Jira REST integration soon, if possible to automate more manual steps

3. Possibly integrate cloning repo in the beginning
