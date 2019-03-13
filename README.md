# LWiki-Linux-Notes





### Configuration


<details> 
<summary> IntelliJ Inotify Watches Limit </summary>
<p> 

Inotify requires a "watch handle" to be set for each directory in the project. Unfortunately, the default limit of watch handles may not be enough for reasonably sized projects, and reaching the limit will force IntelliJ platform to fall back to recursive scans of directory trees.

```
wget  -O /etc/sysctl.d/60-jetbrains.conf "https://gist.githubusercontent.com/bittner/c7d1d49fe0c9af907f24/raw/e2448528477ca3508ad480bea52d3dad54a58f10/60-jetbrains.conf"

sudo sysctl --system
```
</p>
</details>

<details> 
<summary> Apt Autoclean and Clean </summary>
<p> 

```
sudo apt-get update; \
sudo apt-get autoremove; \
sudo apt-get autoclean; \
sudo apt-get clean;
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
<summary> Java Alternatives </summary>
<p> 

```
sudo update-alternatives --config java; \
sudo update-alternatives --config javac; \
sudo update-alternatives --config javadoc; \
sudo update-alternatives --config javap;
```
</p>
</details>
</br>




### Applications
<p align="center">
<img src="https://raw.githubusercontent.com/GensaGames/LWiki-Linux-Helper/master/images/Linux_Apps.png" width="750" height="350" />
</p>
</br>




### Commands
<p align="center">
<img src="https://raw.githubusercontent.com/GensaGames/LWiki-Linux-Helper/master/images/Linux_Commands.png" width="880" height="580" />
</p>
</br>






### Install, Setup

<details> 
<summary> Skype, Slack </summary>
<p> 
   
```
wget https://repo.skype.com/latest/skypeforlinux-64.deb; \
sudo dpkg -i skypeforlinux-64.deb; sudo apt-get update; \
sudo snap install slack --classic; 
```

</p>
</details>


<details> 
<summary> Firefox, Chrome </summary>
<p> 
   
```
sudo apt-get update; sudo apt install firefox; \
sudo wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb; \
sudo dpkg -i google-chrome-stable_current_amd64.deb; 
```

</p>
</details>

<details> 
<summary> Sublime Text3 </summary>
<p> 
   
```
wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -; \
sudo apt-add-repository "deb https://download.sublimetext.com/ apt/stable/"; \
sudo apt-get update; sudo apt-get install sublime-text;
```

</p>
</details>


<details> 
<summary> Java Default, Java 8 </summary>
<p> 
   
```
sudo apt-get update; sudo apt install default-jdk; \
sudo apt install openjdk-8-jdk;
```

</p>
</details>

<details> 
<summary> Git, Global config </summary>
<p> 
   
```
sudo apt update; sudo apt install git; \
git config --global user.name "GensaGames"; \
git config --global user.email "GensaGames@domain.com";
```

</p>
</details>

<details> 
<summary> Py, Py Dependencies and PIP </summary>
<p> 
   
```
sudo apt-get update; sudo apt-get install python3.6; \
sudo apt-get install python3-distutils; \
sudo apt-get install python3-tk; \
sudo apt install python3-testresources; \
wget https://bootstrap.pypa.io/get-pip.py; \
sudo python3 get-pip.py; \
sudo pip3 install pipenv; 
```

</p>
</details>


<details> 
<summary> Minimal Py and PIP </summary>
<p> 
   
```
sudo apt update; sudo apt install python-minimal; \
wget https://bootstrap.pypa.io/get-pip.py; \
sudo apt-get install python-tk; \
sudo python get-pip.py;  \
sudo pip install pipenv;
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
<summary> GIMP </summary>
<p> 
   
```
sudo add-apt-repository ppa:otto-kesselgulasch/gimp; \
sudo apt-get update; sudo apt-get install gimp;
```

</p>
</details>

<details> 
<summary> Intellij Idea (Community) </summary>
<p> 
   
   
```
wget "https://raw.githubusercontent.com/GensaGames/LWiki-Linux-Helper/master/scripts/Intellij-Setup.sh"; \
sudo chmod 777 Intellij-Setup.sh; \
sudo ./Intellij-Setup.sh; 

```
</p>
</details>

<details> 
<summary> Android Studio </summary>
<p> 
   
   
```
wget "https://dl.google.com/dl/android/studio/ide-zips/3.2.1.0/android-studio-ide-181.5056338-linux.zip"; 

```
</p>
</details>

<details> 
<summary> VirtualBox </summary>
<p> 
   
   
```
sudo apt install virtualbox

```
</p>
</details>

<details> 
<summary> Ubuntu Cleaner </summary>
<p> 
   
   
```
sudo add-apt-repository ppa:gerardpuig/ppa; \ 
sudo apt-get update; \
sudo apt-get install ubuntu-cleaner;

```
</p>
</details>
</br>
