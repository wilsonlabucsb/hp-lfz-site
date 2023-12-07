# Local network information

LOKII PC 2 is connected over ethernet to the 7 lasers using a Netgear ethernet bus sitting in the back of the laser rack.
The IP address of the computer is 192.168.3.100 and the IP addresses of the lasers are each 192.168.3.23X where X = 1,2,3,4,5,6,7.
Each IP address is initialized as a "Raw Socket" device in the desktop application "NI-MAX", which creates a "VISA Resource" (think "device") that LabVIEW can communicate with. These VISA Resources are each named "LASERX" were X=1,2,3,4,5,6,7.

It should be noted that the ethernet card on the PC can ONLY be used to connect to the lasers and can't be used to connect to the internet (nor should it be, for safety reasons). Instead, LOKII PC 2 can only connect to internet because it also has a WiFi card. Without this WiFi card, the computer wouldn't have an internet connection.

The IP address of each laser can be modified from the touchscreen on the front panel of the laser unit, by tapping on the IP address at the bottom of the screen and then tapping on the IP address. The first three parts of the IP address must match that of the computer (192.168.3.xxx) in order for the devices to be able to communicate with each other.
