# Kali shell on your linux
For the persons (like me) who searched how to make your shell looks like kali linux. This is not a guide for advanced linux users, but for the linux noobs (like me). Also, i'm french and not yet really good in english, so i do my best to write this in a good english but I apologise for all english errors i'll make.

## Requirements
The default kali shell is **zsh** (Z shell). It's THE shell you must have if you want to have your shell looks like the kali shell.

> To know what shell you're using, open a terminal and copy the command `ps -p $$`:

![how to know what shell you're using](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/zsh.png)

Like you see, in the CMD column there is the name of the shell you're using. Here it's zsh.

## Installation of zsh
  - copy the command `sudo apt-get install zsh`
  - enter your password
  - press "y" if asking
  - Congratulations, you've installed zsh on your computer!

Here's a demonstration:

![install zsh](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/install_zsh.png)

> Now zsh is installed in your computer! to use it, copy the command `zsh` on your terminal (to use a shell, juste type his name on the terminal). But currently, your zsh is probably not very nice! We will change that, but first, we must define zsh as the default terminal. If we don't do that, we will must type `zsh` every time we restart our computer to use zsh and not your default shell.

## Make zsh as your default shell
We'll do this in three steps:
  1. List the shells you have on your computer with `cat /etc/shells` to know what shells you're using
  2. Type the `chsh` command
  3. The command gives the current default shell, and ask you to enter the path to the shells you wants to use by default. This path was indicated by the command you runned in the first step. Here's a demonstration:

![list installed shells](

## Make your zsh look like the kali zsh
To do that, you'll must change your *.zshrc* file (who is stored in your home folder) with a specific code, and also add folders to your */usr/share* directory. This folders and the code for the *.zshrc* files are on this github repository. So we must download the content of this git repository on your computer:
  1.  Open your terminal
  2.  Type `cd` to go on your home folder
  3.  Type `git clone https://github.com/likalium/kali-shell-on-your-linux` to download the content of this repository on your computer
  > If you have an error who say that the git command isn't found, install git with `sudo apt install git` and retry the third step.
  
