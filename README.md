# bash-export
how to move away from foreman for your environment variables and be a sick dev

Step 1 -
create a file in your project root folder called env.sh

Step 2 -
put env.sh in your .gitignore

Step 3 -
PUT ENV.SH IN YOUR .GITIGNORE

Step 4 -
format your file like this:
```
#!/bin/bash
export ENVIRONMENT_VARIABLE_NAME=whatever
export ENV2=etc
export YOU_GET_THE_PICTURE=lol
echo env vars loaded
```
i like to add the echo at the end but it's not necessary

Step 5 -
from the terminal, run
```
$ . ./env.sh
```

Step 6 -
if this doesn't work, run
```
$ chmod 755 ./env.sh
```
and try again
(got that trick from [here](http://ryanstutorials.net/bash-scripting-tutorial/bash-script.php))

Step 7 -
test they loaded by running
```
$ printenv ENVIRONMENT_VARIABLE_NAME
```
or printing/using them in your app
