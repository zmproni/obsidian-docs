# Personal theme setup instructions
## Current Setup

*Figure 1: Theme preview*
![[theme-showcase-2.webp]]

| Technology  |  Theme    | Links |
|---|---|---|
| Openbox | Storm | [pling.com](https://ocs-dl.fra1.cdn.digitaloceanspaces.com/data/files/1552939768/Storm%201.2.1.obt?response-content-disposition=attachment%3B%2520Storm%201.2.1.obt&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=RWJAQUNCHT7V2NCLZ2AL%2F20230111%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20230111T192232Z&X-Amz-SignedHeaders=host&X-Amz-Expires=60&X-Amz-Signature=092e2bdcef02c3ef081c08462ba9e56abb7e89829caf622728226c01eeeb170f) |
| GDK+ | Orchis-Dark | [github.com](https://codeload.github.com/vinceliuice/Orchis-theme/zip/refs/heads/master) |
|Icon Theme | Papyrus-Dark | [github.com](https://codeload.github.com/PapirusDevelopmentTeam/papirus-icon-theme/zip/refs/heads/master) |

## Prerequisite Knowledge
This section will contain prerequisite knowledge needed to understand the following technologies we will use. The inspiration to write this came from a frustration of reading incomprehensible documentations that require a lot of inferred knowledge and a want to be able to recreate the environment need be. Openbox and GDK+ are important in the context of crunchbang++ as they come preinstalled and are the foundation for the Graphical User Interface (GUI) of the operating system.   

### Openbox
X Window System is the windowing system used by Unix-like operating system. Openbox is a manager for that system. Its aim is to be light weight and highly configurable. When configuring Openbox, one is changing the way the window bar looks and the way the pointer menu looks. Additionally you can customise the pointer menu through the menu.xml file. Openbox is a major contributor to the lightweight feel of the CrunchBang++ OS.  

## GTK+
On the other hand, GIMP Toolkit (GTK+) is a multiplatform toolkit used to create graphical user interfaces. Many programs and libraries interface with GTK themes/stylings to augment the look and feel of the app. Changing the GTK theme would affect the looks of applications and system interfaces. 

## Installation
For the installation we will use the GUI provided by CrunchBang++ to change themes. 

### Openbox
Openbox theme manager can be accessed through the Openbox right click menu. Like the name implies it can be opened by right clicking outside of an application or holding the  <kbd>Super</kbd> + <kbd>Space</kbd> keys. 

*Figure 2: Context Menu Navigation*
![[context-menu-openbox.webp | 400 ]]
You can see above, by hovering over `Settings > Openbox > GUI Config Tool`  you can open the theme editor. 

1. Click the link to pling.com to download the file
2. Open the theme editor as shown in *Figure 2* by clicking on GUI Config Tools
3. Press the "Install a new theme" button and select the previously downloaded Storm theme
4. Select Storm in the theme
5. Click close

### GDK+ 

In order to access the GDK+ customization option is that we <kbd>Super</kbd> + <kbd>Space</kbd> and navigate to `Settings > User Interface Settings` .

#### Orchis-Dark Installation
1. Visit the github and download the files as zip or git clone the repo
2. Run the install.sh shell script 
	1. If there are errors encountered with internet connection edit the connection check

#### Icon Theme Installation
1. Visit the github and download the files as zip or git clone the repo
2. Run the install.sh shell script 

#### Change Theme
1. Open the User Interface Settings window
2. Select the widget theme '*Orchis-Dark*'
3. Change default font: System-ui 
4. Change Font size to: 9
5. Navigate to the '*Icon Theme*' bar 
6. Select Papyrus-Dark

## Final Words
After following the above listed steps, your CrunchBang++ environment should look the same as this:

*Figure 3: Theme showcase*
![[theme-showcase-1.webp]]