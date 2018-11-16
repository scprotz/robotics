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

If you have admin rights, it is best if you install python3, pip3, and ssh(openssh) from cygwin.

If you do not have admin rights, then you'll need to get the .zip version of python3.  You will also want to use `putty` instead of ssh.  It is a simple Windows program to do ssh and doesn't require admin rights.

Install Java from the Oracle website.

Use the installer version of Eclipse (not the zip file version).

Install Filezilla if you have admin rights.   If you do not, then get the zip version or dmg version and just run it from there when needed.

#### MAC TBD

It is recommended to install Python3 and Pip3 from homebrew.  Your mac system already has SSH.

Install Java from the Oracle website.

Use the installer version of Eclipse (not the zip file version).

Install Filezilla if you have admin rights.   If you do not, then get the zip version or dmg version and just run it from there when needed.


#### Linux TBD

Python3 will almost assuredly be installed as will pip3.  SSH should be installed too, but if not, install openssh

Install Java based on your Linux version.
 
Use the installer version of Eclipse (not the zip file version).

Install Filezilla if you have admin rights.   If you do not, then get the zip version or dmg version and just run it from there when needed.

```
sudo apt-get install filezilla
```


#### Set up Python3 with Pip3

On a command line (refer back up to your particular installation for help with this), you should be able to run a command like this:

```
pip3 install python-ev3dev2
```

If your installation used the `pip` variation instead of `pip3`, then try it as:

```
pip install python-ev3dev2
```
After it completes, your python environment now has the libraries you'll need to talk to the mindstorm.


#### Set up Eclipse with PyDev

Inside Eclipse, you will need to install the python tools so you can program there.  After you start eclipse, at the top you have the option `Help` and under it `Install New Software`.  Choose that.  It'll bring up a window where you can type in a url.  Put in the url [https://pydev.org/updates]

Once you've done that, you will now have 2 options.  Choose the first one that comes up `PyDev`  You don't need the PyDev Mylyn Integration (optional).

Just click Next.  Accept the terms and conditions and Finish.  Eclipse will restart and you are ready to make a Python3 program.

Once it restarts, you need to choose `File`, `New Project`, and pick a `PyDev project`.  Call it `Hello World`.  

Since this is our first time using Python with Eclipse, we have to tell Eclipse which Python to use.  Click on the link that says `Click here to configure an intrepreter`.  On Mac and Linux it will most likely find it for you.  On Windows, you'll have to navigate to the directory it was installed in.  

Once you've set the python interpreter, Apply it and then Finish creating the project.

### Running a Program

You should be in your `Hello World` project.  Right click on the project and create a new file.  call the file `helloworld.py`

Once the file is open,  type in the following: 


```
print('I am Alive!')
```

Save the file.  Click the Run button (the green arrow at the top of Eclipse).  In the console at the bottom of Eclipse you should see output that says:

```
I am Alive!
```

Congratulations.  Your first Python3 program for Robotics.  Now let's let the Robot do it.


### Make sure the Robot is connected and Run

#### Tethering

If you use a USB cable, when you connect it to the robot and your computer, you'll need to go into the menu on the robot under networking and look under tethering.  Make sure to select the `gadget` option.  This will give the robot an IP address.  You'll need that in a moment to move files over.

#### WiFi

If you have a Wifi adapter for your robot, you need to go into the network settings and connect the robot to your router.  Once it is connected (you may have to enter a password) it will then show you an IP address.  You'll need that in a moment to move files over.

#### Moving Files Over

Start Filezilla.  At the top it has three things to fill in.  The first is the address.  Type
```
sftp://<robot ip address>
```

You'll also need to enter the username and password.  They are the defaults:

```
user: robot
password: maker
```
Do a quick connect.  If it asks you to accept access to the robot the first time, say yes and continue.

On the left hand side you can see your files on your computer.  On the right are files on the robot.  Navigate to your `helloworld.py` file.  Drag it over to the robot.  The file is moved.  Voila!

#### Run the File on the Robot

Start your ssh program (command line or putty for Windows).  For ssh, on a command line type:

```
ssh robot@robot-ip-address
```

It may again ask you to accept.  Say yes.  Enter the password:

```
maker
```

For putty, just fill in the ip address, user name, and password just like on Filezilla.

Once this is done, you should have a console that says something like:

```
robot>
```

You can now run your program by typing:

```
python3 helloworld.py
```

If you get back

```
I am Alive!
```

Then you are all done.  If not, check your steps and try to figure out where it went wrong.  This is good practice for game day so you can react to problems quickly.

### Next Steps
* [Writing a Program to control Motors](Motors.md)
* [Writing a Program to read Sensors](Sensors.md)
* [Reviewing the RCX Challange information](RCX.md)
* [Reviewing World Robotic Olympiad information](WRO.md)


## Authors

* **Dave Mobley**

## License

This project is licensed under the AGPL License - see the [LICENSE](LICENSE) file for details

## Acknowledgments

* EV3DEV community for such wonderful work
