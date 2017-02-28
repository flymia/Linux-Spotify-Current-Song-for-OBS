# SpotCurrent BETA
This simple bash script allows you to get the current spotify-song playing and put it into OBS.

## Installation
### Tutorial
I've made a little tutorial video. Be sure to check it out [here](https://www.youtube.com/watch?v=QND0d5Enzo4).
### Requirements
For this to work, you have to have ```wmctrl``` installed. This is needed to find the window title of Spotify. 
You can install wmctrl by using the command ```sudo apt-get install wmctrl``` .

### Running the script
Download the script and give it the appropriate rights to run (you don't need sudo or anything like that).

```
git clone https://github.com/flymia/Linux-Spotify-Current-Song-for-OBS.git

chmod +x spotcurrent

./spotcurrent
```

### Installing the script
You also can install the application by using the install script located in the source folder.
```
chmod a+x install-spotcurrent
sudo ./install-spotcurrent
```
This will copy the spotcurrent file to the /usr/bin directory, so you can run it anytime.

## Usage
### Running the application
By running the ```spotcurrent``` command, you'll see this output:
```
SpotCurrent v1.0.1 by flymia
Enter your preferred check interval (Press ENTER for default 5 seconds): 
```
As the script writes, enter your desired delay between the song checks. Or just press ENTER for using the default 5 seconds. Every five seconds the script will look for the window title of Spotify and print the information to a file.
```
To abort press CTRL+C
Starting song check...

Current song: MØ - Final Song
```
The script runs now and gives you the information about the current song.

### Reading out the current song
The current song is listed in a file: ```/tmp/currentsong.txt```
You can adjust your OBS for listening a text object on that file. Of course, you can use it with other programs, too.

![Showing the current song with OBS](https://puu.sh/um3fw/5c7ca3cecf.png)

And again: You can use this with other software too. For example showing someone on TeamSpeak to which song you are listening. My application only reads out the current song playing. Nothing more. The rest is up to you!

### Stop spamming the terminal
I recommend you to run this application in a seperate screen. (```sudo apt-get install screen```) Or just open another terminal, if you want to do something else.

## Other stuff
### Future Features
I plan to give this script VLC support, so you can read out every song you're playing on VLC. If you find any bugs, please report them, so I can fix them.

### Important notice
This is just a very basic script. I'm not really fluent in Bash and that's my first "real" script. **It is tested on:**

* Ubuntu GNOME
* Kubuntu (KDE)
* Debian 8 (LXDE)
