# Kali shell on your linux
For the persons (like me) who searched how to make your shell looks like kali linux. This is not a guide for advanced linux users, but for the linux noobs. Also, I'm french and not yet really good in english, so I do my best to write this in a good english but I apologise for all english errors I'll make.

## Note
All the command are made on DEBIAN, so some of them (for example `apt`) will run with DEBIAN-BASED distros. If you have a non debian-based distro (ex: arch linux), you must adapt some commands to your distro.

## Requirements
The default kali shell is **zsh** (Z shell). It's THE shell you must have if you want to have your shell looks like the kali shell.

> To know what shell you're using, open a terminal and copy the command `ps -p $$`:

![how to know what shell you're using](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/know_shell_using.png)

Like you see, in the CMD column there is the name of the shell you're using. Here it's bash.

## Installation of zsh
> if the shell you're using is already zsh, skip this step

  - copy the command `sudo apt install zsh`
  - enter your password (don't care if nothing will appear at the screen when you'll type your password, the computer still see your password so type your password and press enter)
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

Apply the change by moving into your home folder (by doing `cd`) and type `zsh .zshrc`. You shell must look like that:

![zsh of kali](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/kali_zsh.png)

If the colors are differents, that's not a problem, we will configure them.

## Configure the terminal colors
Last step: configure the colors of your terminal. To do that, open your terminal settings. 
> the demonstration will be made with **xfce4-terminal**. I used the name of the packages, so if you want to install them do `sudo apt install qterminal` if you want to use the same terminal as me. If your computer says that the package you want to install is already installed, type the name of the package to lauch it. The demonstrations will be made with **Xfce desktop environnement**.

![open settings in qterminal](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/settings_qterminal.png)

![colors qterminal](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/colors_qterminal.png)

I'll show the hex code for every color in a precise order, so here is a screenshot with a number on every color. I'll change them in this order: 1-2-3-4-5-6-7-8-9-10-11-12-13-14-15-16

![colors qterminal with numbers](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/colors_qterminal_with_numbers.png)

Color 1:

![color 1](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/color1.png)

Color 2:

![color 2](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/color2.png)

Color 3:

![color 3](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/color3.png)

Color 4:

![color 4](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/color4.png)

Color 5:

![color 5](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/color5.png)

Color 6:

![color 6](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/color6.png)

Color 7:

![color 7](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/color7.png)

Color 8:

![color 8](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/color8.png)

Color 9:

![color 9](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/color9.png)

Color 10:

![color 10](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/color10.png)

Color 11:

![color 11](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/color11.png)

Color 12:

![color 12](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/color12.png)

Color 13:

![color 13](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/color13.png)

Color 14:

![color 14](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/color14.png)

Color 15:

![color 15](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/color15.png)

Color 16:

![color 16](https://github.com/likalium/kali-shell-on-your-linux/blob/main/assets/color16.png)


AAAAAAAAAAAAAND IT'S FINISHED! 🥳 GG!
