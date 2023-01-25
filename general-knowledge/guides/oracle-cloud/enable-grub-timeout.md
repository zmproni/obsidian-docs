# Enable GRUB menu on Ubuntu Image on Oracle Cloud
Open the terminal and enter the following command.
```bash
sudo nano /etc/default/grub.d/50-cloudimg-settings.cfg
```
This opens up the GRUB configuration file for the cloud image. Currently, the GRUB timeout is set to 0 leading the GRUB menu not to show. We need to give it an integer greater than 0 and a theme. 
```txt
GRUB_TIMEOUT=5
GRUB_TIMEOUT_STYLE=menu
```
After changing the timeout time and adding a timeout style, we need to update the GRUB settings by running the following line in the terminal. 
```bash
sudo update-grub
```