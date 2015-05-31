# AntergosGnome

Antergos with the latest gnome edition


This is my configuration for Gnome to be used on the Antergos distribution.

I wrote an installation document "read_me_installation_antergos_ base_vx" to cover some specific issues.

Official downloads can be found at 
http://antergos.com/try-it/

Development downloads can be found at
http://build.antergos.com/browse/testing


# What can you achieve?



![Screenshots](http://erikdubois.be/wp-content/uploads/2015/05/achgnome1.jpg)




# A R C H L I N U X   and  A N T E R G O S
-------------------------------------------------

I started using Archlinux as a learning experience. I have tried installing all kinds of desktop environments (DE) and formatted many times my ssd's to start from scratch. Then I started exploring other distro's based on Archlinux. After a while it was more practical to have a script of some kind to record the knowledge and to automate the things I had already learned. They became repetitive in nature.

The goal is to be quickly up and running after a clean install. 

That's why I have written a script to do just that. 

#1. Installation of the ANTERGOS system

Download the iso and burn it on a cd or use a usb.

USB

	sudo fdisk -l
	sudo dd bs=4M if=/path/to/antergos.iso of=/dev/sdX &&  sync


	or

	sudo packer -S imagewriter

Cdrom

	use brasero, xfburn or others

During this installation you will have to choose which graphical environment to choose. 

At the time of writing you can choose

	- base installation (no DE)
	- gnome
	- kde
	- cinnamon
	- mate
	- xfce4
	- openbox

This page is about installing GNOME.

#2. Installation via script

I run an installation script to quickly  get all my software after the installation of Antergos. For me this was quite a learning process, since I was a Redhat, Ubuntu, Linux Mint kind of guy over the last two decades. 

The idea is to download (if you have internet connection) the i3 github files :

	sudo pacman -S git
	git clone https://github.com/erikdubois/AntergosGnome

This folder that you will download will give you all the installation scripts necessary to fully install the desktop.
Change, delete and append whatever you want.

I decided to split the logical entities in seperate files. Better to debug and better for users to understand.

The scripts have been numbered from 1 to 6. Follow the orderering to install all programs.


    

    ./1_install_packer_vx.sh

This will install the program packer. It is a wrapper for yaourt which is already installed. Packer will serve as the aur helper from there on.




    ./2_install_arch_repo _vx.sh

This will install all programs coming from the "normal" arch repositories with the use of pacman.




    ./3_install_aur_repo _vx.sh

This will install all programs coming from the AUR repositories.

If you see a program, you do not want. Just press ENTER and no number and it will be skipped.
In the script you will see a text to know which one you need to choose.

    For example

    echo "################################################################"
    echo "spotify"
    echo "################################################################"

When that is done you run




    ./4_zsh_vx.sh

The zsh script is an alternative for "bash" more colourfull (>100 themes) and more plugins then you ever need.





    ./5_smb_vx.sh

The smb script is to install samba or the way to share folders and files between computers if you need it.




<h2>Give it a go because <b> A N T E R G O S </b> deserves to be more known.</h2>


------------------------------------
#But that is the fun in Linux.

You can do whatever <b>Y O U</b> want.

Share the knowledge.
------------------------------------
