---
layout: post
title: "First time running Raspberry Pi"
date: 2013-09-04 01:21
comments: true
categories: raspberry pi, debian, raspian
---

This is a simple guide to setup Raspberry Pi.
For more advanced and detailed support you can try [the RPi Beginners guide][3].

* * *

To work with raspberry pi, you most likely would need:

* Raspberry Pi :p

  You can get it on [Newegg][8] | [Amazon][21] | [Allied Electronics][24] | [Adafruit][22]. 
  You can also try buying a full [kit at Adafruit][23].
  *Take model B (newer), with or without case (it's up to you).*

* SD card/ micro SD card with SD adapter.

  Anything >= 8 gigs should do
  * [microSDs, Speed Class 10, 8Gbs][9].

  Of course we have to keep in mind that SD memory is not designed to be used so often as hard drives. The SD lifespan, which depends on amount of read/write operations, is much shorter than the other general type of memory. But the rule for SD cards is that the bigger the size of SD memory, the longer SD card will live. But of course you would want to get the card with **good speed rating**. My suggestion is to take 16 GB or more SD card with speed rating of 10. I use [a SanDisk SD card][10] and so far like it a lot for speed and size.

* USB reader for SD cards.

  [You can get it separately][11]  or [together with an SD card][12]. 
  
  *A lot of laptops nowadays has a SD slot so reader is not that necessary.*

* Wireless internet adapter.

 [Edimax EW-7811][13] - a tiny device, but gives a good speed connection
 
 [Rosewill RNX-N180UBE][14] - a little bigger alternative

* [USB hub][15].
  
  If you want more than 2 USB devices connected. For me this is vital, because I need to connect Wi-Fi adapter, keyboard, mouse and a flash drive to Raspberry. A best option is to take hub that is powered over USB. Reason being is that if you want to switch components (plug or unplug USB devices), your Raspberry pi would not reboot. USB Hub provides enough voltage for those devices. On the other hand if you unplug device that is connected straight to the USB port of Raspberry, the voltage spike may occur, causing Pi to reboot :[ 

* Wired USB keyboard/mouse.
 
  [This Logitech mouse & keyboard should do][16].

  *Not all wireless keyboards/mice would work perfect enough with Rapsberry Pi. In fact the wireless keyboard that I used worked so badly that I had to type in pi/raspberry login combination up to 10 times :s On the other hand wireless mouse gave me no trouble, but who knows...*

* microUSB cable.
 
  *Most of you have it already, but if someone don't [here are a few][17]. 
  Make sure it is at least 700mA (0.7A) at 5V. If cable provides less power - it just won't work.*

* [HDMI cable][18] to connect to your monitor.
 
  *Make sure monitor has an HDMI input. When first working with raspberry pi keep in mind that some monitors will have hard time recognizing raspberry pi. [Here sshipway explains the issue][1]. It happened to me on a new ASUS monitor and I had to find another monitor to make it work.
  Additionally if you choose HDMI cable, keep in mind that it carries sound, so you will have one less problem to worry about. :]*

* [Ethernet cable][19].

  *Depends on whether or not you want to connect yours with a cable. You can easily setup a wireless connection on Raspberry Pi*

* Possibly [a heat sink][20].

  *Not that it is "a must have", but pi can get pretty hot (Got it? Oh, yeah...). Any old heat sink would do. Putting pi in front of fan would be just as fine :p*


This is a basic hardware setup for a raspberry pi.

* * *


Now let's go to software! :p

* [RPi Beginners][3] - this will guide you through both the hardware and software.

* [SD Card easy setup - N.O.O.B.S.][4] -
 This is a great instruction set on how to get Raspberry Pi up and running.

 * NOOBS: [Direct Link][5] | [Torrent Link][6]
 * SD Card Formatter: [Direct Link][7]


* After copying NOOBS to your SD card, plug it into Raspberry Pi and boot up!
 
 *Remember to choose a different monitor for Raspberry Pi if it does not work from the start*. 

  If you see nothing, try to hit `2` on keyboard and wait for a few seconds. If you see nothing - try other monitor. Does not help? [Here is another take on this problem][1].

* What OS should I install?

 "RECOMMENDED" or "Raspbian" options are a good choice :p
 <br />


* After Raspbian is installed it will ask you to login. Your default username/password is pi/raspberry . Type in `pi`. Hit Enter. There will be a prompt for password. Type in `raspberry`. Hit Enter. If you fail - remember to use wired keyboard or if it is wireless try another 10 times :s. It should work...hopefully.

* When you are logged in, type in command `startx` and wait a couple of moments.

 At this point you should see a Raspberry Pi image on your screen. 
 To return to command line you can simply hit combination of keys `Ctrl`+`Alt`+`F1`.


* First things:

 * Open up a console again, either locating it on the screen (LXTerminal) or with `Ctrl`+`Alt`+`F1` key combination.
 * On-screen keyboard similar to the one in Windows:
  `sudo apt-get install matchbox-keyboard`
 * Safely eject USB drive command:
  `sudo apt-get install eject`
 * Safely shutdown Raspberry Pi
  `sudo shutdown -t 1 now` and reboot `sudo shutdown -r now`

That's it!

* * *

F.A.Q.

* *If I unplug a USB device from Raspberry Pi, it restarts!*

 This is an expected behavior. It is called '[the rush in current problem][2]'.
 Only use USB hub for plugging in devices that you are going to remove often. Otherwise a sudden voltage spikes will cause Raspberry Pi to reboot. 
 That is why USB hub should have power on.

* *I plug in Raspberry to HDMI monitor and see nothing :(*

 If you are installing Raspian, try hitting `2` (safe mode).
 Otherwise [switch to a different monitor][1], or use an analog cable.

  [1]: http://www.raspberrypi.org/phpBB3/viewtopic.php?f=26&t=34061 "HDMI connection issue"
  [2]: http://www.raspberrypi.org/phpBB3/viewtopic.php?f=63&t=23205 "Rush-in current problem"
  [3]: http://elinux.org/RPi_Beginners "RPi Beginners Guide"
  [4]: http://elinux.org/RPi_Easy_SD_Card_Setup#Using_NOOBS "NOOBS: Easy Setup"
  [5]: http://downloads.raspberrypi.org/images/NOOBS/NOOBS_v1_2_1/NOOBS_v1_2_1.zip "NOOBS: Direct Link"
  [6]: http://downloads.raspberrypi.org/images/NOOBS/NOOBS_v1_2_1/NOOBS_v1_2_1.zip.torrent "NOOBS: Torrent"
  [7]: https://www.sdcard.org/downloads/formatter_4/eula_windows/SDFormatterv4exe.zip "SD formatter: Direct Link"
  [8]: http://www.newegg.com/Product/ProductList.aspx?Submit=ENE&DEPA=0&Order=BESTMATCH&Description=raspberry+pi&N=-1&isNodeId=1 "Newegg: Raspberry Pi"
  [9]: http://www.newegg.com/Product/ProductList.aspx?Submit=ENE&N=40000068%20600006226%20600082443&IsNodeId=1&Description=micro%20SD&name=Class%2010&Order=BESTMATCH "Newegg: SD cards"
  [10]: http://www.newegg.com/Product/ProductList.aspx?Submit=ENE&N=100007796%2050001404%20600082443&IsNodeId=1&bop=And&Order=RATING&PageSize=20 "Newegg: SanDisk High Speed SD cards"
  [11]: http://www.newegg.com/Product/ProductList.aspx?Submit=ENE&N=-1&IsNodeId=1&Description=USB%20Card%20Reader%2FWriter%20For%20SD&bop=And&Order=RATING&PageSize=20 "Newegg: USB Reader standalone"
  [12]: http://www.newegg.com/Product/Product.aspx?Item=N82E16820161590 "Newegg: USB Reader with SD card"
  [13]: http://www.newegg.com/Product/Product.aspx?Item=N82E16833315091&Tpk=ew-7811Un "Newegg: Edimax wireless adapter"
  [14]: http://www.newegg.com/Product/Product.aspx?Item=N82E16833166056 "Newegg: Rosewill wireless adapter"
  [15]: http://www.newegg.com/Product/ProductList.aspx?Submit=ENE&N=40000026%20600000004&IsNodeId=1&Tpk=usb%20hub "Newegg: USB hub"
  [16]: http://www.newegg.com/Product/Product.aspx?Item=N82E16823126097 "Newegg: Logitech wired keyboard + mice"
  [17]: http://www.newegg.com/Product/ProductList.aspx?Submit=ENE&N=-1&IsNodeId=1&Description=microusb%20cable&bop=And&Order=RATING&PageSize=20 "Newegg: microUSB cables"
  [18]: http://www.newegg.com/HDMI-Cables/SubCategory/ID-2809?Tid=16863&cm_sp=Cables197-_-VisNav-_-HDMI%20Cables&Tpk=hdmi%20cable&Order=RATING "Newegg: HDMI cables"
  [19]: http://www.newegg.com/Network-Ethernet-Cables/SubCategory/ID-2825?Tid=16774&Tpk=internet%20cable "Newegg: Ethernet cable"
  [20]: http://www.newegg.com/Product/Product.aspx?Item=N82E16835200042 "Newegg: Heat sink"
  [21]: http://www.amazon.com/gp/product/B009SQQF9C/ref=as_li_ss_tl?ie=UTF8&tag=lifehackeramzn--20&linkCode=as2&camp=1789&creative=390957&creativeASIN=B009SQQF9C "Amazon: Raspberry Pi"
  [22]: http://www.adafruit.com/products/998 "Adafruit: Raspberry Pi"
  [23]: http://www.adafruit.com/products/1014 "Adafruit: Raspberry Pi kit"
  [24]: http://www.alliedelec.com/lp/120626raso "Allied Electronics: Raspberry Pi"
