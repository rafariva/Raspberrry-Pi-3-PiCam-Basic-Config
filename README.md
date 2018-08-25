# Raspberry Pi 3
**PREPARE YOUR RASPBERRY PI** [Step by Step Guide](https://www.raspberrypi.org/documentation/installation/installing-images/)

1. Download the [image](https://www.raspberrypi.org/downloads/) for your raspberry pi
2. Download [Etcher](https://etcher.io/) and install it
3. Connect an SD card reader with the SD card inside.
4. Open Etcher and select from your hard drive the Raspberry Pi file (.img or .zip) you wish to write to the SD card.
5. Select the SD card you wish to write your image to.
6. Review your selections and click 'Flash!' to begin writing data to the SD card (takes between 5 to 10 minutes).

![etcher](/images/etcher.PNG)


**CONFIG YOUR RASPI**

1. Update all libraries (takes between 5 to 10 minutes)
```
sudo apt-get update
sudo apt-get upgrade
```

2. Alias python3 as default
```
alias py=python3
```


3. Run config 'wizard'
```
sudo raspi-config
```
![raspi_config](/images/wizard.PNG)

Most important configuration

1. Option 1 (Password). Important if you want to change your password
2. Option 2 (Network). Usefull to config your wifi network
3. Option 4 (Localisation). Change your Locale, Timezone and Keyboard Layout
4. option 5 (Interfacing). In submenu, Enable what you need (PiCamera, SSH**, VNC?)

Then, Restart your RASPI


**CONFIG PICAMERA** [Step by Step Installation](https://projects.raspberrypi.org/en/projects/getting-started-with-picamera/4)

Enable PiCamera inteface from raspi-config
```
sudo apt-get install python3-picamera
```


**VNC ACCESS** [Step by Step Configuration](https://www.realvnc.com/es/connect/docs/raspberry-pi.html#raspberry-pi-setup) (optional)

Enable VNC inteface from raspi-config
```
sudo apt-get install realvnc-vnc-server
sudo systemctl start vncserver-x11-serviced.service
sudo systemctl enable vncserver-x11-serviced.service
```


