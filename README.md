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
sudo apt-get install python3-pip
```

2. Alias python3 as default
```
alias py=python3
```
on File .bashrc, add: alias py=python3


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

Example Code for taking photo:
```
import picamera
from time import sleep

camera = picamera.PiCamera()
camera.resolution = (640,480)
#camera.framerate = 24
camera.start_preview()
sleep(0.1)

#camera.annotate_text_size = 50
#camera.annotate_text = "Hello world!"
#camera.image_effect = 'colorswap'
#camera.brightness = 70
#camera.contrast = 50

camera.capture('image.jpg')
camera.stop_preview()

```

Example Code for Video:
```
```


**LIBRARIES**

```
pip3 install tensorflow
pip3 install keras
pip3 install requests

pip3 install h5py
pip3 install lxml
sudo apt-get install libxml2-dev
sudo apt-get install libxslt-dev

sudo apt-get install libhdf5-serial-dev
sudo apt-get install libatlas-base-dev
sudo apt-get install libwebp6
sudo apt-get install libtiff5
sudo apt-get install libjasper1
sudo apt-get install openexr
sudo apt-get install libqtgui4
sudo apt-get install libqt4-test
sudo apt-get install libgstreamer1.0-0 gstreamer1.0-plugins-base gstreamer1.0-plugins-good gstreamer1.0-plugins-bad gstreamer1.0-plugins-ugly gstreamer1.0-libav gstreamer1.0-doc gstreamer1.0-tools

```

**VNC ACCESS** [Step by Step Configuration](https://www.realvnc.com/es/connect/docs/raspberry-pi.html#raspberry-pi-setup) (optional)

Enable VNC inteface from raspi-config
```
sudo apt-get install realvnc-vnc-server
sudo systemctl start vncserver-x11-serviced.service
sudo systemctl enable vncserver-x11-serviced.service
```


