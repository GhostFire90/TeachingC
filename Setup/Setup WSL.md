## Why WSL?
WSL stands for *Windows Subsystem for Linux*, basically it lets you setup a linux terminal in your windows powershell. Setting up a development environment in linux is about 1000000x easier than windows

## Actual Setup

First go to "Turn windows Features on or off"  

![WindowsFeatures](<./WindowsFeatures.png>)
  


Setting up WSL is a lot easier than it used to be, as long as you don't have it already installed, all you need to do is run the below command in the powershell program, if you are familiar with linux distros, the automatically installed distro is Ubuntu
```PowerShell
wsl --install
```
if what you see is the default `wsl --help` output than you have run this command once already

Next, you should open a WSL session, easiest way to do this is to just hit the windows key and search wsl and hit enter. It will bring you through a default user creation procedure in which you set the username and password ***KEEP TRACK OF YOUR PASSWORD*** 