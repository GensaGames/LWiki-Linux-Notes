# LWiki-Linux-Helper



### Basics

* [Commands](https://linoxide.com/linux-how-to/linux-commands-brief-outline-examples/) - This article will help you to get familiarized with all the most common Linux commands and their usages. These commands are divided into 15 sections based on their functionalities. Below some examples.


<details> 
<summary> List/Find Proccess </summary>
<p> 

```
sudo ps -ef
```
`ps` - displays processes for the current shell. `-e` - display every active process on a Linux. `-f`- to perform a full-format listing.

```
sudo lsof -t -i:8000
```
`lsof` - list of files(also used for to list related processes). `-t` - show only process ID. `-i` - show only internet connections related process (port in our case). 

</p>
</details>


<details> 
<summary> Killing Process </summary>
<p> 
   
```
# Kill a process by PID
sudo kill <SIG> <PID>

# Kill a process by name
sudo killall <name>
```
   
Possible signals(SIG) for killing.
SIGHUP 1 SIGINT 2  SIGKILL 9, etc. 

</p>
</details>


<details> 
<summary> Change Mode, Access </summary>
<p> 

For the directories only. For the most cases. 
```
find <folder> -type d -exec sudo chmod 755 {} \;
```

Only if you understand, what you are doing.
```
sudo chmod 755 -R <folder>
```

</p>
</details>


<details> 
<summary> Change User Mode </summary>
<p> 

sudo chown <flags> <user-to> <dir>

```
sudo chown -R $USER ./out
```

</p>
</details>



<details> 
<summary> Move(Mv) Command </summary>
<p> 


Mv command main options.`mv -f`	force move by overwriting destination file without prompt. `mv -i`	interactive prompt before overwrite. `mv -u`	update - move when source is newer than destination. `mv -v`	verbose - print source and destination files


Move main.c def.h files to /home/usr/rapid/ directory

```
mv main.c def.h /home/usr/rapid/
```

Move all C files in current directory to subdirectory bak

```
mv *.c bak
```

Move all files in subdirectory bak to current directory

```
mv bak/* .
```

Rename file main.c to main.bak

```
mv main.c main.bak
```

Rename directory bak to bak2:

```
mv bak bak2
```

</p>
</details>


<details> 
<summary> Inotify Watches Limit. IntelliJ </summary>
<p> 

Inotify requires a "watch handle" to be set for each directory in the project. Unfortunately, the default limit of watch handles may not be enough for reasonably sized projects, and reaching the limit will force IntelliJ platform to fall back to recursive scans of directory trees.


```
wget  -O /etc/sysctl.d/60-jetbrains.conf "https://gist.githubusercontent.com/bittner/c7d1d49fe0c9af907f24/raw/e2448528477ca3508ad480bea52d3dad54a58f10/60-jetbrains.conf"

sudo sysctl --system
```

</p>
</details>


<details> 
<summary> IntelliJ. Memmory setting.</summary>
<p> 

`idea.vmoptions` and `idea64.vmoptions`

```
-Xms748m
-Xmx748m
```

`idea.properties`

```
idea.max.intellisense.filesize=999999
idea.max.content.load.filesize=999999
```

</p>
</details>


<details> 
<summary> Apt Autoclean and Clean.</summary>
<p> 


```
sudo apt-get update; sudo apt-get autoremove; sudo apt-get autoclean; sudo apt-get clean;
```

</p>
</details>
</br>



### Apps


* [Startup Disk Creator](https://tutorials.ubuntu.com/tutorial/tutorial-create-a-usb-stick-on-ubuntu#0) - Creating a bootable Ubuntu USB stick is very simple, especially from Ubuntu itself, and we're going to cover the process in the next few steps.



### Install, Setup


<details> 
<summary> Skype, Slack </summary>
<p> 
   
```
wget https://repo.skype.com/latest/skypeforlinux-64.deb; sudo dpkg -i skypeforlinux-64.deb; sudo apt-get update; sudo snap install slack --classic; 
```

</p>
</details>


<details> 
<summary> Firefox, Chrome </summary>
<p> 
   
```
sudo apt-get update; sudo apt install firefox; sudo wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb; sudo dpkg -i google-chrome-stable_current_amd64.deb; 
```

</p>
</details>

<details> 
<summary> Sublime Text3 </summary>
<p> 
   
```
wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -; sudo apt-add-repository "deb https://download.sublimetext.com/ apt/stable/"; sudo apt-get update; sudo apt-get install sublime-text;
```

</p>
</details>


<details> 
<summary> Java Default, Java 8, Update Alternatives </summary>
<p> 
   
```
sudo apt-get update; sudo apt install default-jre; sudo apt install default-jdk; sudo apt install openjdk-8-jdk; sudo update-alternatives --config java; sudo update-alternatives --config javac; sudo update-alternatives --config javadoc; sudo update-alternatives --config javap;
```

</p>
</details>

 
<details> 
<summary> Git, Global config </summary>
<p> 
   
```
sudo apt update; sudo apt install git; git config --global user.name "GensaGames"; git config --global user.email "GensaGames@domain.com";
```

</p>
</details>


<details> 
<summary> Py, Py Dependencies and PIP </summary>
<p> 
   
```
sudo apt-get update; sudo apt-get install python3.6; sudo apt-get install python3-distutils; sudo apt install python3-testresources; wget https://bootstrap.pypa.io/get-pip.py; sudo python3 get-pip.py; 
```

</p>
</details>


<details> 
<summary> Minimal Py and PIP </summary>
<p> 
   
```
sudo apt update; sudo apt install python-minimal; wget https://bootstrap.pypa.io/get-pip.py; sudo python get-pip.py; 
```

</p>
</details>


<details> 
<summary> Tweak </summary>
<p> 
   
```
sudo apt-get install gnome-tweak-tool; 
```

</p>
</details>


<details> 
<summary> Context Option, Empty Document </summary>
<p> 
   
```
touch ~/Templates/Empty\ Document
```

</p>
</details>


<details> 
<summary> Intellij Idea (Community) </summary>
<p> 
   
   
```
wget "https://raw.githubusercontent.com/GensaGames/LWiki-Linux-Helper/master/scripts/Intellij-Setup.sh"; sudo ./Intellij-Setup.sh;

```

</p>
</details>
</br>
