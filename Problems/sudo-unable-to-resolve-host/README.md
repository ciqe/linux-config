# sudo: unable to resolve host explained


https://www.globo.tech/learning-center/sudo-unable-to-resolve-host-explained/

Posted By: GloboTech Communications Jun. 05, 2020

## Unable to resolve host explained.

Sometimes you encounter an error “sudo unable to resolve host”. Usually, this error occurs after changing the hostname of your system. The hostname is the name of your device that the network identifies with. The hostname is stored locally in the file “/etc/hostname”. It is mapped to the network for communication. This is not a big problem and can be solve it easily.

In this tutorial, we will show you how to resolve “sudo unable to resolve host” error.

## Identify the Error

Before starting, we need to identify the actual error with a hostname.

First, check the hostname of your system by running the following command:

```bash 
hostname
```

You should see the following output:

```bash
newpc
```

The above output indicates that the hostname is already setup with your system.

Next, run the following command to reproduce the error:

```bash
sudo
```

You should see the following screen:
Sudo: unable to resolve host explained

As you can see, the message “sudo: unable to resolve host newpc” indicates that the hostname command cannot determine the IP address of host “newpc”

In simple terms, the hostname command cannot resolve the hostname of your system. Since this a local computer and there is no such record in the DNS.
Fix the Error

In order to fix the error, we will need to add the DNS record locally in your system. The local DNS record is stored in the /etc/hosts file.

First, login to root user with the following command:

```bash
su - root
```

if it doesn'twork then:

```bash
sudo -i
```

Next, see the content of the /etc/hosts file using the following command:

```bash
cat /etc/hosts
```

You should see the following screen:
Print /etc/hosts file content using cat command.

As you can see, there is no such record of your hostname (newpc). Since the hostname is missing and your system is not able to figure out the hostname and thus it throws the error ‘sudo: unable to resolve host’.

To fix this error, edit the /etc/hosts file and set the hostname (newpc) with a loopback address (127.0.0.1).

```bash
nano /etc/hosts
```

Add the line “127.0.0.1 newpc” as shown below:
Edit /etc/hosts file content using nano test file editor.

Save and close the file when you are finished. Then, test whether the error is resolved or not with the following command:

```bash
sudo
```

You should see the following screen:
Sudo command without Sudo: unable to resolve host error.

As you can see the error “sudo: unable to resolve host” disappeared.

**[Note : If the old hostname is present in the /etc/hosts file then just replace them with the new hostname.]**

