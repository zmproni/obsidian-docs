# Install radian  
## Purpose
I want to run R on my code editor of choice "VSCode" and be able to run .Rmd files. Radian along with markdown plugins for VSCode allow me to do such. Additionally radian offers a many great features the R console does not provide out of the box. For more information visit the link to the [repository](https://github.com/randy3k/radian) on github. 

## Requirements
- An installation of `R` (version 3.4.0 or above)
- `Python` (version 3.6 or above)
- `pip` (optional)

## [Debian](debian.md) 11
### Installing Python 3
This code verifies the installation of python. Run it before and after running the installation to make sure python is installed correctly. 
```bash
python3 --version
```
If your system does not detect python, you will have to perform your own installation. 
```bash
sudo apt update
sudo apt install python3
sudo apt install python-is-python3
```

### Installing Pip for Python 3
This code verifies the installation of pip. Run it before and after the installation process to confirm pip was installed successfully. 
```bash
pip --version
```
If your system does not detect a pip installation, you will have to perform your own. 
```bash
sudo apt update
sudo apt install python3-pip
```

### Installing R
This section is a rewriting of the original blog post on R installation on Debian systems over at [linuxize.com](https://linuxize.com/post/how-to-install-r-on-debian-10/). 
This code verifies the installation of R. Run it before and after installation to verify the correctlness of the installation process.
```bash
R --version
```

The first step is to install the packages necessary to add a new repository over HTTPS.
```bash
sudo apt install dirmngr apt-transport-https ca-certificates software-properties-common gnupg2
```
Then add the CRAN GPT key to the system and enable the CRAN repository.
```bash
sudo apt-key adv --keyserver keys.gnupg.net --recv-key 'E19F5F87128899B192B1A2C2AD5F960A256A04AF'
```
The code returns an error and depreciation warning. Find issue and fix. As of 12/01/2023 the code will return an error but R will still be installed with the code below. 
```bash
sudo add-apt-repository 'deb https://cloud.r-project.org/bin/linux/debian buster-cran35/'
```
Update the package list and install the R package
```bash
sudo apt update
sudo apt install r-base
```
It is suggested you verify the installation of R after running the above code. 

### Installing the R Ppackages from CRAN
This snippet will install the package that allows for compilation of R packages. 
```bash
sudo apt install build-essential
# Important for installation of future packages like tidyverse
sudo apt-get install r-cran-curl r-cran-openssl r-cran-xml2
sudo apt-get install r-base-dev xml2 libxml2-dev libssl-dev libcurl4-openssl-dev unixodbc-dev cmake
```
This should be the last dependency required before installing radian. 

### Installing radian
```bash
# install released version
pip3 install -U radian

# to run radian
radian
```
If there are any issues runnin radian, its probably because the directory where it was installed is not part of the `$PATH` variable. To add the directory `$HOME/.local/bin`  to the `$PATH$` variable, you can edit your `~/bashrc` file and append the following lines to the file.  

```bash
nano ~/.bashrc
```

```sh
export PATH="$HOME/bin:$PATH"
```

Then you will need to refresh the environment variable to reflect the change. 
```bash
source ~/.bashrc
```
Now you can check again if radian is installed by running the `radian` command in a new terminal. 


