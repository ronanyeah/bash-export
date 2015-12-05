# Exporting environment variables using a bash script.
How to move away from [foreman](https://www.npmjs.com/package/foreman) etc for your environment variables and be a sick dev.

**Step 1**  
Create a file in your project root folder called *env.sh* (or *anything.sh*).

**Step 2**  
Put *env.sh* in your *.gitignore*.

**Step 3**  
PUT *ENV.SH* IN YOUR *.GITIGNORE*.

**Step 4**  
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

**Step 5**  
From the terminal, run: `$ . env.sh`.

**Step 6**  
If it doesn't work, or the printenv doesn't show, run `$ chmod 755 env.sh` and try again.  
(Got that trick from [here](http://ryanstutorials.net/bash-scripting-tutorial/bash-script.php).)

**Bonus**  
On Windows you can use a PowerShell file called `env.ps1` formatted like this to export your variables:
```
Set-Item -path env:TEST_VAR -value 'env vars loaded'
Set-Item -path env:ENVIRONMENT_VARIABLE_NAME -value 'whatever'
Set-Item -path env:PORT -value 8888
Get-ChildItem Env:TEST_VAR
```
You can run the script in a PowerShell terminal with `& .\env.ps1`.
