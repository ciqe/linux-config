# CHANGE HOST NAME IN PARROT LINUX

https://handknitsbybarbara.com/2018/07/16/change-host-name-in-parrot-linux/

<br><br>

When Parrot Linux is installed on a computer, it always names that computer, parrot. That can be very confusing if you have Parrot installed on more than one computer, or you want to have a different name for the computer than the default name. During installation, Parrot does not currently allow the user to specify a specific host name during any part of the installation.
<br>
There are two ways to change the host name.  Since Parrot is Debian-based, and Debian using Systemd for startup and system processes,  Systemd commands can be used, The “new fangled way.”  You can always use the “old fashioned way,” which requires editing the /etc/hosts and /etc/hostname files.  Either method produces the same result.

<br>

### The New Fangled Way

<br>

Changing the host name using Systemd commands is a two-step process.

<br>

*    Open Root Terminal (accessible through the Menu -> System Tools).
*    Enter hostnamectl set-hostname NAME where NAME is the new name for your computer.
*    Close your terminal session, and your computer has been renamed without even having to reboot it.  You can check this by opening a new terminal session.  Looking at the prompt, you’ll see the new host name.

<br>

### The Old-Fashioned Way

<br>

Changing the host name is very easy, but you do have to be careful that that you make sure you don’t assign a name that is currently used on the network. You will have to edit two system files: /etc/hosts and /etc/hostname.

<br>

*    Open Root Terminal (accessible through the Menu -> System Tools).
*    Enter the root password when prompted.
*    On the command line, enter pluma /etc/hosts. You can use any other editor that is on your system if you do not want to use pluma.
*    Locate the line that contains: 127.0.1.1 parrot where hostname is the current name of the computer, parrot.
*    Change host name to whatever you want. You can use letters, numbers, and dash (hyphen).
*    Save the /etc/hosts file and exit pluma.
*    On the command line, enter pluma /etc/hostname.
*    Look for the line that has parrot.
*    Change the host name to whatever you want, but it must be identical to the name you used in /etc/hosts.
*    Save the /etc/hostname file and exit pluma.
*    Exit Root Terminal.
*    Once you reboot your computer, you should see the new name when you open a terminal session or browsing devices on your network.
    
<br>

If you have any comments or notice any error(s) in these instructions, please feel
    free to contact me.
<br>

Barbara

<br>

Updated 7-17-18:  Edited to add hostnamectl instructions.
