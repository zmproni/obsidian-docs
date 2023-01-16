# Important commands

## $ apt install \[options\] \[package\] 
```bash
apt install [options] [package]
```
Searches for package, downloads it and installs it onto the system. 

## $ ls \[options\] \[directory\]
Lists files in a given directory

## $ which \[options\] \[program\]
```bash
which [program]
which git
which python
```
Returns the path to the application 

## $ source ~/.bashrc
```bash
source ~/.bashrc
. ~/.bashrc
```
Reloads bashrc without restarting the terminal

## $ \[command\] $(...)
```{bash}
cd $(echo $JAVA_HOME)
```
Make use of echos as input for other commands

