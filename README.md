
 
 
# Rpi Video Looper
Make your Raspberry Pi loop a video file endlessly and seamlessly, without showing any logo or breaks.
A simple, cheap and reliable media player/digital signage solution that just works. No configuration needed. This solution is using the pi_video_looper script, all installed and configured. If you don't have the time, or the desire, or the means to learn to code it yourself, this is for you.

Original project can be found here: https://github.com/adafruit/pi_video_looper

# Instructions

Currently only the Legacy version of Raspberry Pi OS Lite is supported. You can download it from here: <br>
[raspios_oldstable_lite_armhf-2022-01-28/2022-01-28-raspios-buster-armhf-lite.zip](https://downloads.raspberrypi.com/raspios_oldstable_lite_armhf/images/raspios_oldstable_lite_armhf-2022-01-28/2022-01-28-raspios-buster-armhf-lite.zip)

Connect your Rpi to your network and power it on. If your using a Rpi Zero, be sure to enable wifi and ssh. More info here: https://desertbot.io/blog/headless-pi-zero-w-wifi-setup-windows 

When the Rpi has booted up, log in using:

       user: pi
       password: raspberry 

Now it's time to get into the good stuff. 

Type/Paste in one line at the time: 

       sudo apt-get update
       
       sudo apt-get install -y git
       
       sudo git clone https://github.com/adafruit/pi_video_looper
       
       cd pi_video_looper
       
       sudo chmod +x install.sh
       
       sudo ./install.sh
Done!
Now shut down your Rpi with:

       sudo shutdown -h now
       
When the Rpi is off, load your USB-stick with your favorite videos and enjoy! :)


# Configuring

To change some settings of the Video Looper, either pull the SD-card out and put it into your computer or use SSH.

Computer:

       Edit video_looper.ini which is located in the root of the SD-card.
SSH:

       Type sudo nano /boot/video_looper.ini to make changes. Press CTRL+X when your done followed by Y then ENTER.

More about the Video Looper settings can be found here: https://learn.adafruit.com/raspberry-pi-video-looper/usage
       
       
# Troubleshooting

When using the Raspberry Pi ZERO, you might want to use the Analog audio only. Using both HDMI and Analog audio out will cause stuttering because the Rpi ZERO is not powerful enough. You can change this in the `video_looper.ini` which is explained above:

       #sound = both
       #sound = hdmi
       sound = local













