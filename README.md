# laravel-basics
using framework laravel

download and install virtualbox and vagrant

use git bash as the terminal, and to install laravel on virtualbox


////////////////////////////////////////////////////////////////////////////////////////////////
http://sherriflemings.blogspot.ca/2015/03/laravel-homestead-on-windows-8.html
Laravel Homestead on Windows 8
Posted by Sherri Flemings | File under : code, development, Homestead, Laravel 5, PHP, Vagrant, Windows 8
Install Laravel Homestead 2.0 on Windows
I've tried to set up Laravel's Homestead on Windows a few times before. Until now I always gave up because I just ran out of time trying to troubleshoot one error after another on both of my Windows machines. The Homestead setup guide and Laracast videos make it look so freaking easy, but they are not targeting Windows users so it sometimes becomes a very frustrating experience for us... and usually ends with reverting back to your XAMPP or WAMP installation and a promise to try again when you have more time.
I finally had some time to try this again, and although there were a lot of steps and some annoying errors it was actually pretty easy to get going! I know there are some web devs out there who might be intimidated using a command-line, or a virtual machine and some of the error messages you get might have you feeling like you're in way over your head but I wanted to break it down here for you step by step and explain some of the errors to help you get over the initial hurdle of installing Homestead on your Windows machine.
Warning - Before you begin you should verify in your system's BIOS that Intel Virtualization Technology is enabled. It will save you some troubleshooting time if you check now before you get started.
My goal is to install and setup Laravel 5 and Homestead 2.0 on my Windows 8.1 machine. I will be following the same steps on the Laravel install page,  but I will change the paths for Windows and share any errors I came across.
Dependencies:
Before we start make sure you have installed the following software:
Git Bash (Git for Windows) 
Vagrant
VirtualBox
Bitvise Tunnelier (or Putty if you prefer)
Before you install Vagrant - Vagrant uses Ruby, and there is a known issue with Ruby and spaces in paths. My very first mistake was to change the Vagrant install location to %ProgramFiles% like a good Windows citizen and that was a spectacular failure. I opted to install it here on my machine: C:\Tools\Vagrant. I just do my best not to cringe when I see that clutter in the root of my system drive.
Step 1: Open Git Bash
I highly recommend that you use Git Bash as your command-line for the following steps since it will allow us to enter the same commands in the docs without having to manually edit files. If you are also planning to install the vagrant hostsupdater plugin, make sure you open Git Bash as an administrator:


Step 2: Add Vagrant Box
Verify that you have the recommended Vagrant version for Homestead which at the time of this post was Vagrant 1.6
Git Bash
$ vagrant version
Add the Laravel Homestead Box to Vagrant
Git Bash
//////////////////////////////////////////////
$ vagrant box add laravel/homestead
/////////////
This will take several minutes so feel free to grab a coffee or a sandwich depending on your Internet speed.


If download stops, clear the temp file this way:
Git Bash
////////////////////////
rm ~/.vagrant.d/tmp/*  
//////////////

$ vagrant box add laravel/homestead

////////////////
