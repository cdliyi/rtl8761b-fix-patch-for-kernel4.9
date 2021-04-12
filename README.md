# rtl8761b-fix-patch-for-kernel4.9

This patch is just simply replace rtl8761a to rtl8761b.

discuss thread: https://discourse.coreelec.org/t/rtl8761b-bluetooth-driver-fix/15286

# Build CoreELEC in a docker container

## Pull the image and run the container
- docker pull coreelec/coreelec-builder:latest
- docker run -v ~/:/home/docker -h coreelec -it coreelec/coreelec-builder:latest


## Clone repo and build image inside container
- git clone git://github.com/CoreELEC/CoreELEC.git ~/CoreELEC
- cd ~/CoreELEC
- cp linux-09-rtl8761b-fix.patch to ~/CoreELEC/projects/Amlogic-ng/patches/
- time(PROJECT=Amlogic-ng ARCH=arm make image)

Use PROJECT=Amlogic to build images for older S912 and S905/X/D devices
