# raspberrrypicam
**PREPARE YOUR RASPBERRY PI** [Step by Step Guide](https://www.raspberrypi.org/documentation/installation/installing-images/)

1. Download the [image](https://www.raspberrypi.org/downloads/) for your raspberry pi
2. Download [Etcher](https://etcher.io/) and install it
3. Connect an SD card reader with the SD card inside.
4. Open Etcher and select from your hard drive the Raspberry Pi file (.img or .zip) you wish to write to the SD card.
5. Select the SD card you wish to write your image to.
6. Review your selections and click 'Flash!' to begin writing data to the SD card (takes between 5 to 10 minutes).


**CONFIG YOUR RASPPI**

1. Update all libraries (takes between 5 to 10 minutes)
```
sudo apt-get update
sudo apt-get upgrade
```
2. Run config 'wizard'
```
sudo raspi-config
```




**VNC ACCESS** [Step by Step Configuration](https://www.realvnc.com/es/connect/docs/raspberry-pi.html#raspberry-pi-setup)
2. sudo apt-get install realvnc-vnc-server
3. sudo raspi-config. --> navigate to Interfacing Options > VNC and select 'Enabled' or 'Yes'
4. sudo systemctl start vncserver-x11-serviced.service
5. sudo systemctl enable vncserver-x11-serviced.service


**CONFIG PICAMERA** [Step by Step Installation](https://projects.raspberrypi.org/en/projects/getting-started-with-picamera/4)
1. sudo raspi-config. --> navigate to Interfacing Options > Camera and select 'Enabled' or 'Yes'
2. sudo apt-get install python3-picamera
