### The systemd Controversy

Author: **Spandan Ghosh** </br>
Contact me : <br/>
https://www.linkedin.com/in/spandanghosh2/<br/>
https://github.com/another-dark-knight/

<br/>

The Linux world has changed rapidly in the past few years. It has become beginner friendly with proper hardware support requiring little or no technical knowledge to get up and running. There are several Linux(more accurately GNU/Linux) distributions out there Debian, Fedora , Arch Linux, Gentoo, Solus, Clear OS, Gentoo and many more. One thing that most of these distros have in common is *Systemd* (Gentoo primarily supports and ecourages OpenRC but has systemd profiles as well). My 11 years of linux usage has taught me to both respect and hate systemd and today hopefully I can convince you of the same. While I myself am not a big fan of systemd I will try to(If I can) be as objective as possible so as to not enforce an opinion on you. <br/>
<br/>
To love or hate something we must understand what it is. Systemd is an **init** system. And now coming to the basic question whose answer shall shape the approach we take to come to the controversy that systemd is. 
<br/><br/>
**What is an init system? What is is supposed to do?**<br/>
Let us walk through how our machine would boot. The boot process starts with the BIOS (Basic Input / Output System) which looks at the bootable disks and attempts to open up a bootable hard disk. This is usually a bootloader which gives us a menu of chices regarding what to boot. A popular bootloader is **grub**, The booloader would then look for the Linux kernel selected (Happy to see I am not considering a Windows boot as an option XD). Right ahter the kernel loads and the driver loading scripts are executed, the init system is started. As the name suggests it initiates and runs a bunch of services as requested by the user. Eg: It may run a service that enables ssh access to the system. The handling of these services is the task of the init system.
<br/><br/>
Usually this init system is run as the first process and is hence PID 1 of the system. In the older days, Linux used to use SysVInit as the init system before systemd came along. It made service management extremely simple. I am not going to list the commands here. Fire up your terminal emulator of choice and run the following to just begin to know how much you use systemd without actually knowing (In case you still use a distro that sets a lot of things up for you)<br/>
```
$ man systemctl
$ man journalctl
```
!['Systemd Components']('/spandan/linux/systemd/Systemd-components.png')
Systemd is on many modern hardware considerably faster than SysVinit and does a lot more. It has its own poewer management scripts, an excellent binary logging system and many more features. It does all that an **init** system must do and more. It is basically the paradise for someone who does not want to worry about much and get going with his/her workflow. There are also scripts to anlalyze your boot time and do in something called a critical-chain, all of which you will find in the man pages.
<br/>
<br/>
While we are in the *heaven* that systemd is, we have maybe gone a bit astray as to what we, the Linux community represent. We represent respect for opinions of the people and have always encouraged the ability of people to choose. Now assume that you are an.
<br/>
<br/>
With all these features (jargon), Systemd is no longer just an init system. It does a lot og things for you and if you are a minimalist like me, it does way too much than it should. For a hardcore minimalist, **Systemd is bloat**. I would just like to clarify here that I like what systemd does for someone who does not care what the init does and just wants everything to work while focussing on one's respective project or other (lesser crazy) aspects of life.

