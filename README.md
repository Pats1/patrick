# patrick
***DWSservice***

after burning Image 32bit.

Open a terminal and run these commands:

sudo raspi-config

Go to Advanced and disable Wayland.

sudo reboot

cd /usr/src

sudo wget -N https://www.dwservice.net/download/dwagent.sh

sudo chmod +x dwagent.sh

sudo ./dwagent.sh

***Remove dwagent***

 sudo /usr/share/dwagent/native/dwagsvc stop

 sudo /usr/share/dwagent/native/dwagsvc delete

 sudo rm -r -f /usr/share/dwagent

 sudo rm -f /etc/dwagent

***RPITX***

sudo apt-get update

sudo apt-get install git

git clone https://github.com/F5OEO/rpitx

cd rpitx

./install.sh

Plug a wire on GPIO 4, means Pin 7

easytest is the easiest way to start and see some demonstration. 

cd rpitx

./easytest.sh

***Hamclock***
curl -O https://www.clearskyinstitute.com/ham/HamClock/install-hc-rpi
chmod u+x install-hc-rpi
./install-hc-rpi
If you chose not to install a desktop icon, you can run HamClock from the terminal at any time by typing this command:
hamclock &

***WSL** (schrink images)

CMD as Administrator
wsl --install -d Debian

Open the Debian app from your start menu
sudo apt update && sudo apt install -y wget parted gzip xz-utils udev e2fsprogs
wget https://raw.githubusercontent.com/Drewsif/PiShrink/master/pishrink.sh
chmod +x pishrink.sh
sudo mv pishrink.sh /usr/local/bin

Your C:\ drive is mounted at /mnt/c/

Usage: pishrink.sh [-adhnrsvzZ] imagefile.img [newimagefile.img]

  -s         Don't expand filesystem when image is booted the first time
  -v         Be verbose
  -n         Disable automatic update checking
  -r         Use advanced filesystem repair option if the normal one fails
  -z         Compress image after shrinking with gzip
  -Z         Compress image after shrinking with xz
  -a         Compress image in parallel using multiple cores
  -d         Write debug messages in a debug log file


cd /mnt/c/'Documents and Settings'/patss/Downloads

sudo /usr/local/bin/pishrink.sh startl_demoUSR_demo.img startl_demoUSR_demo_reduced.img
		
