# PulseAudio manual switcher - HDMI or Analog to Laptops and PCs with buggy switching in the Distro's interface (wat a big name)
I was having problems with the HDMI audio output in my laptop using an external monitor on my Linux distro (I use Mint with XFCE and MX Linux), so I made this script to sort the problem out.

The purpose of this script is to allow an user to switch the PulseAudio output when this does not work on the Linux Distro interface (my case) in a simple command line. 

### What it does?
It runs the pactl command (pulseaudio control) and changes the output to either HDMI or Analog audio.

### Where it works?
I successfully tested this in Linux Mint with XFCE in this moment. 
As of hardware: Intel HD4000 Graphics. Since the Linux Kernel has the Intel graphics drivers built on it by default if you're using an Intel processor this should probably work to you. AMD devices too. 
But this bug happens (to me) in Intel devices alone for who knows what reason.

### How to?
Well, just clone this repo somewhere on your system.  You can run the command on the repo's folder to switch the audio output. 
For example: to HDMI audio:
```bash
./switchaudio hdmi
./switchaudio h
```
And for integrated  output audio:
```bash
./switchaudio integrated
./switchaudio i
```

**Sidenote:** if you run the command on a terminal with no parameter, you'll be presented with an interactive screen to choose which audio output to switch to.

### I'm a lazy bastard, I don't wanna go to the repo folder to run the command. What should I do?
Well, we got you covered. Make sure the repo is in a place that you won't delete and run the script:
```bash
./addToBin
```
This will make a symbolic link to the system's bin folder to the command **switchaudio** and the shorthand command **sad**. Then you'll be able to run it with a run command (usually alt+f2 on distros) or even set a shortcut in your window manager to make the audio output tweak. Your ability to tweak is the limit :)

(**Note:** To run addToBin you'll be asked your user's password. Make sure you have permissions to run sudo commands)

So after running the above script you should be able to run this globally with no problem:

```bash
sad hdmi
switchaudio h
sad i
switchaudio integrated
```

### Contributing
Want to improve this? Make a pull request and get in touch :)
This is such a simplistic piece of code that I doubt it is even useful to someone else, but who knows ^^

### Licensing
MIT? Yeah, MIT.

