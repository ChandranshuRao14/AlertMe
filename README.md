# alertme
alertme is a Python-based command-line tool that allows developers to get gmail notifcations of their scripts that are running. Simply use the command alertme along with your script, type in your email, and alertme will take care of the rest.

## Usage
alertme is installed via PyPI. To install alertme simply:
```
pip install alertme
```    
To use alertme with a script:
```
alertme myScript.py
```
Currently alertme only works with bash and python scripts. For more information about this read the options below.

## Options
alertme comes with some built-in options

### Bash
The [-b ] option sets the script type as a bash script. The default script type for alertme is python.
```
alertme -b myScript.sh
```    
### Subject
Option [-s] allows the user to input the Subject of the email notification that will be sent to the user.
```
alertme -s myScript.py
```    
### Output
The output option [-o] redirects myScript's STDOUT to a file. If myScript contains an error, the STDERR will be outputted to a file as well.
```
alertme -o myScript.py
```    
STDOUT will be outputted to myScript.py.AlertMe.out.txt
    
STDERR will be outputted to myScript.py.AlertMe.err.txt

If myScript has/throws an error, both the out.txt and the err.txt files will be attached to the notification email. Otherwise just the output file will be attached.

The output option also works with bash as well.
```
alertme -b -o myScript.sh
```
## Troubleshooting
For alertme to work properly:
* myScript must be in the **current working directory**
* myScript must have a .py or .sh extension. A .sh extension must accompanied with the [-b] option 

## Issues
alertme is still in very early stages of development and therefore many bugs or issues may occur. Known issues that need to be fixed include:
* myScript must be in the current working directory
* alertme cannot attach large output files to emails. Unfortunately there doesn't seem to be a workaround this.

## Contributing
I'm still fairly new to Python so feedback would be greatly appreciated. PRs would be awesome too. I'm always striving to become a better programmer so if you have any improvements or critiques I'm all ears!
