# VERSION 3.0

Author: Matt Proctor

Creation: 2022-01-15

Version 3.0 differs from 2.0 as it automates more of the bug fixing process, including:
	Automatically running jira jql query to avoid manual copying and pasting.

## IN PROGRESS:
1. Normal cherry-picking COMPLETE
2. Get CHLRQ of issue
3. Get CHLC of challenge (jira REST api?)
4. Get Parent CHLC (jira REST api?)
5. Auto transition CHLRQ
6. Auto link CHLRQ in CHLC
7. Bulk transition all CHLC's, assign Thomas, comment link to CHLRQ (Change from manual to auto)
8. Remind user to go into the CMS to update files

## Setup and usage Help:
1. Save this file in /usr/local/bin so you can call it from anywhere
2. Call this from inside of the repo after you have made the fix
3. VSCode will be opened whenever a merge conflict is encountered
4. Press Enter to continue after you have resolved the conflict
5. Automatically opens up CHLC jql query in your browser
