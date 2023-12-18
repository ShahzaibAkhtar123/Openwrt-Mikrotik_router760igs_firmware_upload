


apt update 
apt upgrade
reboot

apt install build-essential ccache ecj fastjar file g++ gawk gettext git java-propose-classpath libelf-dev libncurses5-dev libncursesw5-dev libssl-dev python python2.7-dev python3 unzip wget python-distutils-extra python3-setuptools python3-dev rsync subversion swig time xsltproc zlib1g-dev

//if error than use 2nd command

sudo apt install build-essential ccache ecj fastjar file g++ gawk gettext git default-jdk libelf-dev libncurses5-dev libncursesw5-dev libssl-dev python2.7-dev python3 unzip wget python3-setuptools python3-dev rsync subversion swig time xsltproc zlib1g-dev




git clone https://git.openwrt.org/openwrt/openwrt.git

cd openwrt



---------------------------------if you want to checkout some specific branch other than master ------------------
git branch -a
git tag
git checkout v23.05.0
check Makefile for the links.
------------------------------------------------------------------------------------------------------------------
 
 ./scripts/feeds update -a
 ./scripts/feeds install -a
 
 if you get warning try these commands 
 
 ./scripts/feeds update -i -f
 
 -i (or --include-missing):
This option tells OpenWrt to include missing feeds during the update process. It can be useful when you have feeds that are not present or enabled in your current configuration, and you want to update them.

-f (or --force-refresh):
This option forces a full refresh of the package feeds. Even if the feeds were recently updated, using this option ensures that OpenWrt retrieves the latest package information from the feeds.


make menuconfig
here a screen open where you can customize your firmware.after save the .conf file.
run this command make -j4



I already make configuration file and place in the same folder with the name of Mikro_tik_23.05.0 ....
you can use this file and replace this file with the name of .conf in your openwrt folder and than run make -j4
Or
build your own firmware as we discuss in early steps..


