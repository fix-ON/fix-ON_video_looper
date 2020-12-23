
 
 
# Fix-ON Video Looper
This is a translated version (Swedish) of the original Adafruits pi video looper. Only the on-screen texts in the scripts are translated, everything else is the original creators code. Credits goes to them!

Original project can be found here: https://github.com/adafruit/pi_video_looper

# Instructions

Download and flash your SD-card with the latest version of Raspbian Lite: http://downloads.raspberrypi.org/raspbian_lite/images/

Connect your Rpi to your network and power it on. If your using a Rpi Zero, be sure to enable wifi and ssh. More info here: https://desertbot.io/blog/headless-pi-zero-w-wifi-setup-windows 

When the Rpi has booted up, log in using:

       user: pi
       password: raspberry 

Overclock the Rpi with (this can't be done with Rpi ZERO's):

       sudo raspi-config
    
       Overclock > Press “OK” > Medium
       
Press Finish when your done:

Now it's time to get into the good stuff. 

Type/Paste in one line at the time with: 

       sudo apt-get update
       
       sudo apt-get install -y git
       
       sudo git clone https://github.com/fix-ON/Rpi_video_looper.git
       
       cd Rpi_video_looper
       
       sudo chmod +x install.sh
       
       sudo ./install.sh
Done!
Now shut down your Rpi with:

       sudo shutdown -h now
       
When the Rpi is off, load your USB-stick with your favorite videos and enjoy! :)


# Configuring

To change some settings of the Video Looper, either pull the SD-card out and put it into your computer or use SSH.

Computer: 
Edit `video_looper.ini` which is located in the root of the SD-card.
<br>SSH:
Type `sudo nano /boot/video_looper.ini` to make changes. Press `CTRL+X` when your done followed by `Y` then `ENTER`.

More about the Video Looper settings can be found here: https://learn.adafruit.com/raspberry-pi-video-looper/usage
       
       
# Troubleshooting

When using the Raspberry Pi ZERO, you might want to use the Analog audio only. Using both HDMI and Analog audio out will cause stuttering because the Rpi ZERO is not powerful enough. You can change this in the `video_looper.ini` which is explained above:

       #sound = both
       #sound = hdmi
       sound = local













