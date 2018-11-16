# Robotics Team for Winburn Middle School

This is the home page for the robotics team for Winburn Middle School.  On here you'll find some quick getting started tips on how to work with the Lego Mindstorms and EV3DEV and also how to set up your computer.  If you have any issues, put a note in the Issues section and hopefully someone will be be able to provide a quick answer.

## Getting Started

So the first thing you'll need to do is get all the equipment you will need and a computer to work on.  So here are the assumptions that we'll start with:

1)  You need to have a Lego Mindstorms EV3 block (the computer part of it)
2)  You need a computer to work from.  I'll try to give reasonable instructions for the 3 main platforms (Windows, Mac, and Linux)

*) You'll need a good internet connection and this can be kind of a pain depending on how locked down your laptop is and if you have wifi or not for your robot.

### Setting up EV3DEV on your robot.

Here are the quick steps:

1)  Download EV3DEV to your computer from [https://github.com/ev3dev/ev3dev/releases/download/ev3dev-stretch-2018-08-06/ev3dev-stretch-ev3-generic-2018-08-06.zip](https://github.com/ev3dev/ev3dev/releases/download/ev3dev-stretch-2018-08-06/ev3dev-stretch-ev3-generic-2018-08-06.zip)

2)  You need to put that on a Micro-SD card.  To do that, you need a program called Etcher.  You can get Etcher at [https://www.balena.io/etcher/](https://www.balena.io/etcher/).  Get the version appropriate for your Windows/Mac/Linux computer.

3)  Install Etcher and run it.  Use a Micro-SD from 8GB-32GB for your ev3dev image.  IT WILL BE ERASED.  Let me say that again.  IT WILL BE ERASED.

4)  Etcher will asked for an image.  Unzip the one from step 1.  On some computers this might be called 'extract'.  Just extract it somewhere that you know (like your Downloads folder).  Point Etcher to it.  Also when Etcher asks, point it to the SD card.  This will make an EV3DEV image for your Mindstorms.  Make sure to tell Etcher to burn it.


WooHoo!  Take the Micro-SD and put it in your Mindstorms and start it.  You should be all set.

### Setting up your computer

For our team, we are going to start with Python3.  To get Python3 working on your computer the way we will all use it, you will need to install the following software (If you do not have administrator priviliges on your computer, this should all still work, but there may be extra steps to get it working just right).

1) Python3
2) Pip3
3) Java (version 8 or higher - 8 is recommended)
4) Eclipse
5) Filezilla
6) SSH

Wow - That is a lot of software.  Let's review WHY we need all that software.

1)  You need to install Python3 because this is the language we'll be programming in.
2)  Pip3 is needed to add stuff to your Python (like the ev3dev libraries that let us talk to things like motors and sensors)
3)  Java is needed because we are going to use the Eclipse framework  (there are other options, but Eclipse works great and gets the job done)
4)  Eclipse is where we will be programming stuff, mainly our Python3
5)  Filezilla is a nice little file-mover program.  It is very useful when moving files to your mindstorms robot because you can just drag and drop
6)  SSH is for when you really just need to get on the robot and run stuff directly.  It will start up a command line for you to work on the mindstorms.

#### Windows TBD

#### MAC TBD

#### Linux TBD


#### Set up Python3 with Pip3

#### Set up Eclipse with PyDev


### Running a Program

At this point, the assumption is that you have the robot running EV3DEV and your computer is up and running with Eclipse.

```
Give the example
```

## * Save this page as a Cheat Sheet
## * Save this page as a Cheat Sheet


## Authors

* **Dave Mobley**

## License

This project is licensed under the AGPL License - see the [LICENSE](LICENSE) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
