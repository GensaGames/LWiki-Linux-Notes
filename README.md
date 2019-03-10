# LWiki-Linux-Helper





</br>
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
</br>
</br>



<p align="center">
<img src="https://coggle-downloads-production.s3.eu-west-1.amazonaws.com/217fcb67d6552e2d63e332ed2fc6bcc77f8466c5d4150a389126ceccf3ed1838/Linux_Commands.png?AWSAccessKeyId=ASIA4YTCGXFHD56ZGW64&Expires=1552241879&Signature=Fkf6H8vTAT1zYuLn6fpHnU04fZk%3D&x-amz-security-token=FQoGZXIvYXdzENX%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaDGGszEl1NRsii4p8zyLwAbLTimhhsWFS%2FH8Jlk8N5Cz27STAo0Hh8D9kTGE5UGLBBJM2S%2BfIIY2ssEFuKabAB3QvHrmjIv8CyaWGbuegGodSxFNrR%2BkbkNdk0faU0qmBXLSm7odlz8MzEn2sNNlx6D16mxr59mNzFnbMNWc2XOzSidXocDCDONcl0IWYuSsx4027NaQpuBrbFpHnF3Ku4U6Sw%2FaZeTN4PufiIYZngm1edurg%2BTJlojuDJgl9lFAuyA%2FbSKfnMAIZ24bDqa%2BQnjQnmwCQbJ8vcKQlAu%2BrsgAXiuTbT5mdsXcZh9%2B0Q8%2F6SOyiNuuCDfmh7zYyghNOjCi14ZPkBQ%3D%3D" width="700" height="400" /> 
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
<summary> Java Default, Java 8, Update Alternatives </summary>
<p> 
   
```
sudo apt-get update; sudo apt install default-jdk; \
sudo apt install openjdk-8-jdk; \
sudo update-alternatives --config java; \
sudo update-alternatives --config javac; \
sudo update-alternatives --config javadoc; \
sudo update-alternatives --config javap;
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
<summary> Context Option, Empty Document </summary>
<p> 
   
```
touch ~/Templates/Empty\ Document
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
</br>
