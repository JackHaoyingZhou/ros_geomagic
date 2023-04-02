Description
---------

ROS Interface for Geomagic Touch Haptic device

## Original Author (Phantom Omni Interface)
Dane Powell
https://github.com/danepowell/phantom_omni.git

## Authors (Conversion from Phatom Omni to Geomagic Touch)
Hai Nguyen, Marc Killpack, Chi-Hung King, Sven Bock, Prof. Charlie Kemp
https://github.com/HumaRobotics/geomagic_touch

## Extended Author and Maintainer
Haoying Zhou, Adnan Munawar

# Geomagic

## How to install

```bash
git clone --recursive https://github.com/JackHaoyingZhou/ros_geomagic.git
```

All required files are in `driver_install` folder. Therefore, firstly go to  `driver_install` folder. 

Then, you may install the driver via running following command:

```bash
cd 3ds-touch-openhaptics
sudo ./install-3ds-openhaptics-3.4.sh
sudo ./install-3ds-touch-drivers-2019.sh
```

** Note, please make sure that you are installing the touch driver with 2019 version. The latest version may lead to non-reading issue.

## How to run
After you build the package with ROS, you can run it as

```bash
roslaunch geomagic_control geomagic_headless.launch
```
This should start streaming the ROS topics with the states of the device.

# Potential Alternative Solution for Phantom Omni

## Ubuntu 16.06, 18.04 and 20.04:
First, please install the Openhaptics SDK from this location:

https://github.com/jhu-cisst-external/phantom-omni-1394-drivers

### Known Issues
For Phantom Omni, you may need admin priviliges to access the device. The simplest way is to run the following command in your terminal.
```
sudo chmod a+rw /dev/fw*
```
Then you can try rerunning the roslauch command above.

### Deprecated:
```
sudo ln -s /usr/lib64/libPHANToMIO.so.4.3 /usr/lib/libPHANToMIO.so.4
sudo ln -s /usr/lib/libPHANToMIO.so.4 /usr/lib/libPHANToMIO.so
sudo ln -s /usr/lib/libPHANToMIO.so.4 /usr/lib/libPhantomIOLib42.so
```
