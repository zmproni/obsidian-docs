# How to set up SSH key authentication for GitHub on a Debian OS

## Purpose 
I made this article to document the steps taken to setup GitHub authentication with SSH on my CrunchBang++ (#!++) OS I recently switched to.

## Steps
1. Generate a key
```bash
ssh-keygen -t ed25519 -C <email-address> 

# You can chose to specify a different directory and/or file name using the -f 
ssh-keygen  -t ed25519 -C <email-address> -f /path/to/my_rsa_key
```
By default if you don't specify a path and name for your file with the `-f` option, then the private ssh key generated will be found in the   `~/.ssh/` directory with the default name of `id_ed25519` and its public key counterpart with the same name but with a `.pub` file extension. 

2. Make sure to start SSH Agent 
```bash
ssh-agent -s
```

3. Edit the .ssh/config file
```
ls ~/.ssh/
```
Make sure all the previous files were created correctly and are present in the folder you defined. 

```bash
# if the file exists you can skip this line 
touch ~/.ssh/config
```

Open the file with your text editor of choice. In this example I am using nano. 
```bash
sudo nano ~/.ssh/config
```

Once the file is opened, enter the following text:
```bash
Host *
  AddKeysToAgent yes
  IdentityFile ~/.ssh/id_ed25519
  UseKeychain yes # Optional 
```
The Identity file should point to your private ssh key. If you changed the name and location of where the key was generated, insert the path to that file after `IdentityFile` . Use Keychains is an optional setting that can be omitted if you don't want to use password authentication on top of SSH authentication.   

Once you're done, save and exit the file. 

4. Enter your public key into Github 
To add a new SSH key on GitHub, go to [https://github.com/settings/ssh/new](https://github.com/settings/ssh/new) or login and navigate to your account settings, under "SSH and GPG keys" click on "New SSH key" button.

**Title**: stands for the name you want to give the key, it is up to you how you decide to identify your SSH keys. Eg: The name of your machine. 

**Key type**: Authentication Key. Should not be changed for the purposes of this tutorial. 

**Key**: Here, you will be required to enter the contents of your public ssh key. Since I did not define a specific name for my public key, the key in question is `~/.ssh/id_ed25519.pub` .

If you're not sure how to view and copy the contents of the file, you can use the cat command:
```bash 
cat ~/.ssh/id_ed22519.pub
```
Then copy the output and paste it onto Github. 
Once you're done filling up the form, click the Add SSH key. 

5. Make sure everything is working as intended
```bash
ssh -T git@github.com
```
If this is your first time connecting to GitHub using ssh (it should be, if you're reading this guide), then you should get a confirmation prompt to continue connecting. Type yes and press enter. If you get a congratulatory message, saying you've successfully authenticated, but GitHub does not provide shell access, then ssh has been set up correctly. 

From now on, when you clone, pull, push, etc... you will have the ability to authenticate with the GitHub servers using your SSH key. 