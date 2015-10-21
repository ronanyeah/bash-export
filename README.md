# Exporting environment variables using a bash script.
How to move away from foreman for your environment variables and be a sick dev

Step 1 -  
Create a file in your project root folder called env.sh (or anything.sh).

Step 2 -  
Put env.sh in your .gitignore.

Step 3 -  
PUT ENV.SH IN YOUR .GITIGNORE.

Step 4 -  
Format your file like this:
```
#!/bin/bash
export TEST_VAR='env vars loaded'
export ENVIRONMENT_VARIABLE_NAME=whatever
export ENV2=etc
export YOU_GET_THE_PICTURE=lol
printenv TEST_VAR
```
The `printenv TEST_VAR` isn't necessary but I like to add it to give me some feedback that they have loaded correctly.

Step 5 -  
From the terminal, run: `$ . env.sh`.

Step 6 -  
If it doesn't work, or the printenv doesn't show, run `$ chmod 755 env.sh` and try again.  
(got that trick from [here](http://ryanstutorials.net/bash-scripting-tutorial/bash-script.php))
