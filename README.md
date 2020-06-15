# Enable Remote Access to Raspberry Pi-OctoPi Using VNC
After we've successfully setup OctoPi on our Raspberry Pi, we will see how to use VNC to control our Raspberry Pi from another computer, so you can use your OctoPi without a screen, mouse or keyboard! 

(P.S. : It's very easy)

A quick and easy guide to setting up OctoPi for beginners with zero experience. Follow these steps to setup OctoPi OS on your Raspberry Pi in a few basic steps regardless of your machine's operating system.

![Octopi image](https://user-images.githubusercontent.com/64366648/84556016-58e23580-ad20-11ea-9105-232916981913.jpg)

![vnc](https://user-images.githubusercontent.com/64366648/84674897-d4fc9900-af2b-11ea-9b1c-be0ee10a852d.png)

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

![1](https://user-images.githubusercontent.com/64366648/84674994-f2316780-af2b-11ea-9f01-396d8d1bb1ad.png)

Enter your password

* Select "5 Interfacing Options"

![2](https://user-images.githubusercontent.com/64366648/84675044-01181a00-af2c-11ea-879c-980b4b54b191.png)

* Select "P3 VNC"

![3](https://user-images.githubusercontent.com/64366648/84675092-10976300-af2c-11ea-8791-62401a115eb7.png)

* Select "Yes"
  
![4](https://user-images.githubusercontent.com/64366648/84675132-2016ac00-af2c-11ea-92f3-0ca782f889f1.png)

* Authorise it by typing "Y" and hitting enter

![5](https://user-images.githubusercontent.com/64366648/84675254-463c4c00-af2c-11ea-8ef2-466700144105.png)

The resources for VNC will now install
You will see a message saying that VNC Server is enabled

![6](https://user-images.githubusercontent.com/64366648/84675337-679d3800-af2c-11ea-89ff-b106f0d45ccf.png)

* Select "Finish"
  
![7](https://user-images.githubusercontent.com/64366648/84675379-7683ea80-af2c-11ea-9250-5a5d7fa6025b.png)

* You will now notice a new VNC icon in the top-right corner of the screen.

![8](https://user-images.githubusercontent.com/64366648/84675426-83a0d980-af2c-11ea-861c-7eb844c49b61.png)

* Right click on the VNC icon and click on "Options.."

* Enter your password.

* Change the Authentication from UNIX password to VNC password.

![9](https://user-images.githubusercontent.com/64366648/84675470-961b1300-af2c-11ea-93dd-bf17aa1dd20f.png)

* Click "Apply"

Now, we specify the new VNC password.

![10](https://user-images.githubusercontent.com/64366648/84675585-be0a7680-af2c-11ea-8c67-9bbfd5219b10.png)

* Click "OK"

The VNC server is now sucessfully setup.

We now need to find out our Raspberry Pi's local IP address.

In the bash terminal, type:

>> ifconfig

You can now see your IP address. (wlan0: inet ---.---.-.--)

![11](https://user-images.githubusercontent.com/64366648/84675710-edb97e80-af2c-11ea-8823-91dfff217e17.png)

We will need this IP address shortly..


### Setting up VNC on our desktop/laptop (Server Side):

Now we need to install a VNC client on our system.

https://www.realvnc.com/en/connect/download/viewer/

Download and install VNC client as per your system OS.
Open VNC viewer on your system.

* In the address bar, enter the IP address of your Raspberry Pi

![Image 15-06-20 at 4 27 PM](https://user-images.githubusercontent.com/64366648/84675860-1e011d00-af2d-11ea-86ee-450febae03a9.jpeg)

* When prompted, Enter the password

![Image 15-06-20 at 4 28 PM](https://user-images.githubusercontent.com/64366648/84675917-2c4f3900-af2d-11ea-8e0c-6ae0d13f23f3.jpeg)

#### Your Octopi is now successfully remotely connected to your System! You can now remote control your Raspberry Pi - OctoPi. You can now disconnect your Raspberry Pi from the monitor, mouse and keyboard!

## Next: How to control your 3D printer using OctoPi:

Stay tuned...

## Meta

**Harshit Shandilya - https://www.linkedin.com/in/harshitshandilya/ 

Affero General Public License (AGPL)

https://github.com/shandilyaguy247

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b`)
3. Commit your changes (`git commit -am`)
4. Push to the branch (`git push origin`)
5. Create a new Pull Request
6. For major changes, please open an issue first to discuss what you would like to change.
