# DWServiceOnSlackware

Install DWService on Slackware 14.2

# Download

```
cd
wget https://www.dwservice.net/download/dwagent_generic.sh
```

# Install

```
chmod +x dwagent_generic.sh
su
./dwagent_generic.sh
```

Here is the console output

```
./dwagent_generic.sh
Extracting file ...
Running installer ...

****************************************
Commands:
 #BACK <enter> to go back.
 #EXIT <enter> to exit.
****************************************

License
This software is free and open source.
It consists of one main component and several accessory components defined "app" that could be governed by different licenses. For more informations visit: https://www.dwservice.net/en/licenses-sources.html

Security
To protect your privacy we guarantee that no information will be stored on our servers and communications are encrypted so third parties can't read them anyway.

Software updates
The updates of this software are automatic.

1. Install
2. Run
3. I do not accept
Option (3): 1
Waiting...

Select the installation path:
Path (/usr/share/dwagent):
Waiting...

Do you want install DWAgent to '/usr/share/dwagent'?

1. Yes
2. No
Option (2): 1
Waiting...
Folder creation...
Downloading file config.xml...
Downloading file files.xml...
Downloading file agentupd_linux_x86_64.zip...
Downloading file agent.zip...
Downloading file agentui.zip...
Downloading file agentapps.zip...
Downloading file agentui_linux_x86_64.zip...
Downloading file agentlib_linux_x86_64.zip...
Copying files...
Installing service...

Error: Installation service failed.
Press enter to continue.
```

So, it crash ! _Installation service failed._
Don't panic. Quit the script with CTRL-C and let's go ;)

# Install rc script

Copy my `rc.dwservice` script in your `/etc/rc.d/`.

Change permissions :

`chmod 755 /etc/rc.d/rc.dwservice`

Now you can start DWService :

`/etc/rc.d/rc.dwservice start`

By the way, I suggest to add this line to your `/etc/rc.d/rc.local`. So DWService will start after a reboot...


# Configure

Of course, you are now able to configure DWService :

`sh /usr/share/dwagent/native/configure`

Enjoy ;)






