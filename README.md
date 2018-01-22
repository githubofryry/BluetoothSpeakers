# Speaker Bonnent

![Image of Speaker Bonnet](https://github.com/githubofryry/BluetoothSpeakers/blob/master/documentation/IMG_4650.JPG?raw=true)

## Table of Contents
1. [Introduction](#introduction)
2. [What you will need](#what-you-will-need)
3. [Assembly](#assembly)
4. [Software Setup](#software-setup)


### Introduction

The Speaker Bonnet is a stereo amplifier for the Raspberry Pi. This Speaker Bonnet is used for audio for any UNIX-like OS.
This build instruction will teach you how to build your own Speaker Bonnet!
For the music player, we will be using mpg123 for this project. 

### What you will need

What will you need for this:

![A raspberry pi](https://github.com/githubofryry/BluetoothSpeakers/blob/master/documentation/IMG_4651.JPG?raw=true)

**WARNING: Be sure to use a 2.5A/5V if you will be using 4W 3ohm speaker or using 2 speakers on the Speaker Bonnet. It is not recommended to use a charging brick that does not have the power to do so. This could damage your Pi.**

[Link for the raspberry pi](https://www.amazon.ca/CanaKit-Raspberry-Complete-Starter-Kit/dp/B01CCF6V3A/ref=sr_1_5?s=electronics&ie=UTF8&qid=1516598053&sr=1-5&keywords=raspberry+pi+3)

If you already have a micro SD card and do not care about the case then you could just buy the Raspberry Pi itself.


[Link](https://www.amazon.ca/Raspberry-Pi-RASPBERRYPI3-MODB-1GB-Model-Motherboard/dp/B01CD5VC92/ref=sr_1_4?s=electronics&ie=UTF8&qid=1516598053&sr=1-4&keywords=raspberry+pi+3)

Speaker Bonnet
![Speaker Bonnet](https://github.com/githubofryry/BluetoothSpeakers/blob/master/documentation/IMG_4652.JPG?raw=true)

Either a 8ohm 1W speaker ![8ohm 1W speaker](https://github.com/githubofryry/BluetoothSpeakers/blob/master/documentation/IMG_4653.JPG?raw=true) 
or 4ohm 3W speaker 

(Will be using the 8ohm 1W for this project)

[Link for the 8ohm 1W speaker](https://www.adafruit.com/product/1313)
[Link for the 4ohm 3W speaker](https://www.adafruit.com/product/1314)

2 Jumper Cables
![2 Jumper Cables](https://github.com/githubofryry/BluetoothSpeakers/blob/master/documentation/IMG_4654.JPG?raw=true)

2 Alligator clips
![2 Alligator clips](https://github.com/githubofryry/BluetoothSpeakers/blob/master/documentation/IMG_4655.JPG?raw=true)



### Assembly

First what you will need to do is solder the parts given to your the speaker bonnet. If you are not confident on 
soldering then I would suggest to watch youtube videos on it first before attempting to solder. 
[Soldering Tutorial](https://www.youtube.com/watch?v=AqvHogekDI4)

Now when you know how to solder, go ahead and solder the 20 pin and the right/left terminals on the back of the border.
I suggest to do this one part at a time and take your time soldering.
It should look like this when completed.

![Pic1](https://github.com/githubofryry/BluetoothSpeakers/blob/master/documentation/IMG_4656.JPG?raw=true)

![Pic2](https://github.com/githubofryry/BluetoothSpeakers/blob/master/documentation/IMG_4657.JPG?raw=true)

Once the Speaker Bonnet is soldered, then you can now start hooking it up to the Pi and Speakers.

Insert the Speaker Bonnet on the 20pin of the Raspberry Pi
![Pic3](https://github.com/githubofryry/BluetoothSpeakers/blob/master/documentation/IMG_4658.JPG?raw=true)
![Pic4](https://github.com/githubofryry/BluetoothSpeakers/blob/master/documentation/IMG_4659.JPG?raw=true)

Then get the jumper cables, plug them accordingly into the terminal, and then screw them in (+ = red jumper, - = black jumper | You can use any colour but I recommend using red and black for quality of life). If you are able to obtain 2 speakers then add the 2nd speaker on the other terminal.
![Pic5](https://github.com/githubofryry/BluetoothSpeakers/blob/master/documentation/IMG_4660.JPG?raw=true)

Now get your alligator clips and plug them accordingly (red = positive, black = negative). 
![Pic6](https://github.com/githubofryry/BluetoothSpeakers/blob/master/documentation/IMG_4661.JPG?raw=true)

Grab the speaker you will be using (mines the 8ohm 1W) and connect it to the positve and negative with the other end of the alligator clips.
![Pic7](https://github.com/githubofryry/BluetoothSpeakers/blob/master/documentation/IMG_4662.JPG?raw=true)
![Pic8](https://github.com/githubofryry/BluetoothSpeakers/blob/master/documentation/IMG_4663.JPG?raw=true)


Now once you have everything connected, you can do the software setup!

### Software Setup

Now install Raspbian on your Pi (I already have it installed but here is a [video](https://www.youtube.com/watch?v=GJDIgS8nres) on that). If you bought the CanaKit Raspberry Pi, Raspbian should be already on the SD card. All you would need to do is connect it to Wi-Fi or Ethernet internet connection in order to get it installed.

Once you are on Raspbian, you can either press Ctrl + Alt + T for the terminal or click the black box that has a blue header and inside of it has >_.

![Pic9]()

Now that you are on the terminal, you will need the scripts to install the drivers for the Speaker Bonnet. The scripts I used are the one on adafruit. You can however do an advanced version yourself if you know what you are doing. 
So this is what you will be entering on the terminal.

curl -sS https://raw.githubusercontent.com/adafruit/Raspberry-Pi-Installer-Scripts/master/i2amp.sh | bash

![Pic10]()

Since I already installed the driver, it should ask to reboot your Pi after installing. 

Once the Pi is rebooted, you should now be able to use the speakers. Now go back to your terminal and download mpg123 which is
the media player for the Pi. 

type in the terminal: sudo get-apt install -y mpg123

![Pic11]()

Now once you are done, you should be able to play your music now via mp123. But if you are going to use your own music, then
I suggest you either transfer the music files onto the SD card via USB Transfer so that you do not have to download anything on the Pi. 
(Be sure that the files do not have spaces and they are replaces with dashses like this -. The reason I say this is because when we go on the terminal and have to type the song name, you will see how difficult it will be since spaces on UNIX based operating systems are not the same as on Windows Operating systems.)

 
