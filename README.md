# Enable Remote Access to Raspberry Pi-OctoPi Using VNC
After we've successfully setup OctoPi on our Raspberry Pi, we will see how to use VNC to control our Raspberry Pi from another computer, so you can use your OctoPi without a screen, mouse or keyboard! 

(P.S. : It's very easy)

A quick and easy guide to setting up OctoPi for beginners with zero experience. Follow these steps to setup OctoPi OS on your Raspberry Pi in a few basic steps regardless of your machine's operating system.

![Octopi image](https://user-images.githubusercontent.com/64366648/84556016-58e23580-ad20-11ea-9105-232916981913.jpg)
! (https://github.com/shandilyaguy247/Enable_Remote_Access_to_Raspberry_Pi-OctoPi_Using_VNC/issues/1#issue-638925836)

So what exactly is VNC? 

VNC, or Virtual Network Computing, is a system allowing remote control of one computer by another. When using VNC, two different parts of the software are used.
The first part is the VNC server. This one is installed on the machine we want to take control of (here the raspberry pi), and it will allow the connection and the control by the client part.
The second part is therefore the VNC client. It is installed on the machine from which you wish to control the server (your laptop/desktop) and it will allow to translate your actions into operations comprehensible by the server which will then control the remote machine from your computer.

The main interest of VNC is that it allows to take control of a remote machine, while displaying the desktop of it. So you can see in real time what is happening on your Raspberry Pi, without having to plug it into a screen, mouse or keyboard!

## Installation

### Prerequisites:

Here we are already assuiming that you have sucessfully installed OctoPi GUI on your Raspberry Pi machine. If you haven't done so yet, please check out the previous tutorial here: 

https://github.com/shandilyaguy247/OctoPi_GUI_Setup/blob/master/README.md

* Raspberry Pi (Model 3B or later) with OctoPi GUI installed.
* USB Mouse and Keyboard
* Monitor 
* HDMI cable
* 5.1V/2.5 A Micro USB power supply (For the RPi)
* Stable Wifi
* Desktop/Laptop

### Setting up VNC on the Raspberry Pi (Server Side):

#### We will now enable remote desktop operation using VNC server

* Open the bash terminal.

Type:

>> sudo raspi-config

(I1)

Enter your password

* Select "5 Interfacing Options"

(I2)

* Select "P3 VNC"

(I3)

* Select <Yes>
  
(I4)

* Authorise it by typing "Y" and hitting enter

(I5)

The resources for VNC will now install
You will see a message saying that VNC Server is enabled

(I6)

* Select <Finish>
  
(I7)

* You will now notice a new VNC icon in the top-right corner of the screen.

(I8)

* Right click on the VNC icon and click on "Options.."

* Enter your password.

* Change the Authentication from UNIX password to VNC password.

(I9)

* Click "Apply"

Now, we specify the new VNC password.

* Click "OK"

The VNC server is now sucessfully setup.

We now need to find out our Raspberry Pi's local IP address.

In the bash terminal, type:

>> ifconfig

You can now see your IP address. (wlan0: inet ---.---.-.--)

(I11)

We will need this IP address shortly..


### Setting up VNC on our desktop/laptop (Server Side):

Now we need to install a VNC client on our system.

https://www.realvnc.com/en/connect/download/viewer/

Download and install VNC client as per your system OS.
Open VNC viewer on your system.

* In the address bar, enter the IP address of your raspberry pi

* When prompted: Enter the password

#### Your Octopi is now successfully remotely connected to your System! You can now remote control your Raspberry Pi - OctoPi. You can now disconnect your Raspberry Pi from the monitor, mouse and keyboard!

## Next: How to control your 3D printer using OctoPi:

Stay tuned...

## Meta

**Harshit Shandilya - (https://www.linkedin.com/in/harshitshandilya/ **

Affero General Public License (AGPL)

https://github.com/shandilyaguy247

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b`)
3. Commit your changes (`git commit -am`)
4. Push to the branch (`git push origin`)
5. Create a new Pull Request
6. For major changes, please open an issue first to discuss what you would like to change.
