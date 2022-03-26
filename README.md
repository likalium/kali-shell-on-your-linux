# Kali shell on your linux
For the persons (like me) who searched how to make your shell looks like kali linux. This is not a guide for advanced linux users, but for the linux noobs (like me). Also, i'm french and not yet really good in english, so i do my best to write this in a good english but I apologise for all english errors i'll make.

## Requirements
The default kali shell is **zsh** (Z shell). It's THE shell you must have if you want to have your shell looks like the kali shell.

> To know what shell you're using, open a terminal and copy the command `ps -p $$`:

![how to know what shell you're using](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/know_shell_using.png)

Like you see, in the CMD column there is the name of the shell you're using. Here it's bash.

## Installation of zsh
> if the shell you're using is already zsh, skip this step

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
  2. Type the `chsh` command then enter your passsord
  3. The command gives the current default shell, and ask you to enter the path to the shells you wants to use by default. This path was indicated by the command you runned in the first step. Here's a demonstration:

![list installed shells](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/list_shells.png)

![chsh](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/chsh.png)

## Make your zsh look like the kali zsh
To do that, you'll must change your *.zshrc* file (who is stored in your home folder) with a specific code, and also add folders to your */usr/share* directory. This folders and the code for the *.zshrc* files are on this github repository. 

### Clone this repository on your computer

So we must download the content of this git repository on your computer:
  1.  Open your terminal
  2.  Type `cd` (that moves you in your home folder)
  3.  Type `git clone https://github.com/likalium/kali-shell-on-your-linux` to download the content of this repository on your computer
  > If you have an error who say that the git command isn't found, install git with `sudo apt install git` and retry the third step.
  
  ![install git](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/install_git1.png)
  
  ![clone repository](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/install_git2.png)
  
  
  
  After doing that, move you on the folder chere are stored all the elements of this repository with `cd kali-shell-on-your-linux`.
  
  ![cd kali-shell-on-your-linux](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/cd_kali-shell-on-your-linux.png)
  
  ### Move the zsh-autosuggestions & zsh-syntax-highlighting folders
  - Your actually on a folder who contain folders and files you'll must move at the right place.
  - First, do `ls`to see the files and folders there is here, like of this example:

![ls in kali-shell-on-your-linux](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/ls.png)

You can see two folders, one named **zsh-autosuggestions** and one named **zsh-syntax-highlighting**. You must move it in the `/usr/share` directory.
  1.  Type `sudo mv zsh-autosuggestions /usr/share` and type your password.
  2.  Type `sudo mv zsh-syntax-highlighting /usr/share` and type your password.

![mv folders](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/mv.png)

This folders are now at the right place. Now we must configure zsh.

### Configure the .zshrc file
The **.zshrc** file store the "design datas" of zsh, and he's stored in your home folder. So if the kali zsh is so unique, it's because of his highly sophisticated **.zshrc**.
You will replace your actual **.zshrc** by the **.zshrc** who is here, by doing this:
  - `cat zshrc > ~/.zshrc`
> `~` is a shortcut who is equivalent to your home directory

![cat zshrc > ~/.zshrc](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/cat_zshrc.png)
