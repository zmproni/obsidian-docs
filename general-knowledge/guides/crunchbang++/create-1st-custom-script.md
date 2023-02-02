# Your first custom Linux terminal script 
Ever thought, hey I wonder how I can write my own 'cd' command, or I want to conviniently perform a git sync operation with one command. Well, it is possible; afterall, someone must have written all those commands we already use before. Here's what you need to know:
## Command file
The command will have to be written as a file, in bash, without a file extention, and the name of the file needs to be the name of the command. For example, I want to write a command "say-hello" that prints "Hello world!" into the console. 
```bash
touch hello-world
nano hello-world
```
I would create a file called say-hello, then enter the following lines in it:
```bash 
echo Hello world!
```
Save and exit <kbd>Ctrl</kbd> + <kbd>S</kbd> , <kbd>Ctrl</kbd> + <kbd>X</kbd>. Afterwards, we need to change the properties of this file so that we allow the f({
	
})ile to be run as a program. We can do this in the terminal though the following command:
```bash
chmod u+x say-hello
```
## /usr/bin
This directory is the directory where the file will have to be placed in. If you want to run the command anywhere in any working directory like standard linux commands, then you'll have to place the  file in this directory. 
```bash
mv say-hello /usr/bin/say-hello
```
Now that the file in the `/usr/bin` directory, we can open the terminal from any directory and run:
```bash 
say-hello
```
And with that, we're done creating our first simple command. 

For custom languages and more information, this link may be of use:
https://stackoverflow.com/questions/2177932/how-do-i-execute-a-bash-script-in-terminal