# Kali shell on your linux
For the persons (like me) who searched how to make your shell looks like kali linux. This is not a guide for advanced linux users, but for the linux noobs (like me). Also, i'm french and not yet really good in english, so i do my best to write this in a good english but I apologise for all english errors i'll make.

## Requirements
The default kali shell is **zsh** (Z shell). It's THE shell you must have if you want to have your shell looks like the kali shell.

> To know what shell you're using, open a terminal and copy the command `ps -p $$`:

![how to know what shell you're using](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/zsh.png)

Like you see, in the CMD column there is the name of the shell you're using. Here it's zsh.

## Installation of zsh
To install zsh, copy the command `sudo apt-get install zsh` (for the complete noobs: the `apt-get` command install packages from the **official repositories**), type your password if asking, and press y (for "yes"). Here's a demonstration:

![install zsh](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/install_zsh.png)

> Now zsh is installed in your computer! to use it, copy the command `zsh` on your terminal (to use a shell, juste type his name on the terminal). But currently, your zsh is probably not very nice! We will change that.

## Make your zsh look like the kali zsh
To do that, you'll must change your *.zshrc* file (who is stored in your home foler) with a specific code, and also add folders to your */usr/share* directory. This folders and the code for the *.zshrc* files are on this github repository. So we must download the content of this git repository on your computer. For this, create a folder where you want to store the content of this repository. After that, go on your terminal and type `cd
