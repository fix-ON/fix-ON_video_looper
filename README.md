# Fix-ON Video Looper

This is a translated version (Swedish) of the original Adafruits pi video looper. Only the on-screen texts in the scripts are translated, everything else is the original creators code. Credits goes to them!

Original project can be found here: https://github.com/adafruit/pi_video_looper

#Instruction
Flasha ett SD-kort med senaste Raspbian Lite versionen: https://www.raspberrypi.org/downloads/raspbian/

Koppla in nätverkssladd och strömsätt Raspberry Pi’n.

När Raspberry Pi’n  har bootat upp och stannat. Logga in med uppgifterna:

user: pi 

pass: raspberry

Konfiguera Raspberry Pi’n med:
sudo raspi-config
För automatisk inloggning:
Boot Options > Desktop / CLI > Console Autologin
Överklocka en smula:
Overclock > Tryck “OK” > Medium
Avsluta och starta om.


När konsolen scrollat klart och loggat in automatiskt, skriv in dessa rader:
sudo apt-get update
sudo apt-get install -y git
sudo git clone https://github.com/fix-ON/Rpi_video_looper.git
cd Rpi_video_looper
sudo chmod +x install.sh
sudo ./install.sh
Klart!
Starta om din Raspberry Pi och sätt in ett USB-minne laddat med filmer. 
 
 

