# Installing a VNC Server

## VNC

Virtual Network Computers allow you to remotely control computers over a network. VNC is a flexible protocol that has led to the creation of a number of powerful free and paid-for applications

##TightVNC

Accoring to their <a href="http://tightvnc.com/" target="_blank">website</a>:

What is TightVNC?

TightVNC is a free remote control software package. With TightVNC, you can see the desktop of a remote machine and control it with your local mouse and keyboard, just like you would do it sitting in the front of that computer. TightVNC is:

 - free for both personal and commercial usage, with full source code available,
 - useful in administration, tech support, education, and for many other purposes,
 - cross-platform, available for Windows and Unix, with Java client included,
compatible with standard VNC software, conforming to RFB protocol specifications.

With TightVNC, you can:

 - cut your expenses and save your time on traveling,
 - help your friends and family to solve problems with their computers remotely,
 - make sure nothing wrong is happening on your computers when you are away.

### Installation

To install TightVNC Server on your Raspberry Pi Simply run the following command:

```bash
 sudo apt-get install tightvncserver
```

Click <kbd>Y</kbd> on your keyboard to agree and install.

![Command Line](http://domhnallohanlon.github.io/rpi/img/server00.png "Installation Command")


### Running 

The first time to run tightvncserver you will be prompted to enter an 8 character password.

![run](http://domhnallohanlon.github.io/rpi/img/server01.png "Run tightvncserver")

![pw](http://domhnallohanlon.github.io/rpi/img/server02.png "Set password")


###Autostart
Now that we have the ability to allow remote desktop access it would be great if we could start tightvncserver automagically, thereby eliminating the need to ever plug our Pi into a screen in the first place. Click on the image below for a screencast of how to achive this.

[![asciicast](https://asciinema.org/a/24902.png)](https://asciinema.org/a/24902)

### That's All Folks!

You don't have to specify a view-only password if you don't want to. Make a note of your VNC name, typically a number between 0 and 4. In the example below it's `raspberrypi:1`

![running](http://domhnallohanlon.github.io/rpi/img/server03.png "X is now running.")


That's everything you need to do to get tightvncserver running on your Raspberry Pi. If you know your IP address you can take remote control of your Pi using [a VNC client](mdwiki.html#!00vncclient.md). If you're not sure of your IP you should probably [SSH in](mdwiki.html#!00putty.md) and run `ifconfig` to find out. 



## Summary

To go back to the chapter overview click [here](mdwiki.html#!00overview.html)

To return to the Raspberry Pi Recipes page click [here](https://domhnallohanlon.github.io/rpi)