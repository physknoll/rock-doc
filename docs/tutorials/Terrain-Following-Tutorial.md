# LiDAR Acquisition with Ground Control Points

## Intro

After you have completed the
getting started tutorial and you have your ROCK R1A mounted to your drone and
powered on for the first time, you can jump into this lesson. This lesson will
walk you through the steps of collecting and processing a LiDAR survey with Ground
Control Points.  For this tutorial we are using the ROCK R1A on the DJI M210 Drone
with the EMLID Reach RS2 survey kit and ground control aerial targets. (A complete list
of equipment used is below)  

This tutorials will cover the following:

* Capturing Ground Control Points
* Terrain Following flight plan
* Pre flight and Post flight LiDAR Calibration
* Uploading Data to the ROCK cloud
* Generating Bare Earth Digital Elevation Model (DEM)
* Generating Contours
* Viewing and Downloading Results

Lets jump right in!

## Prerequisites

* Completed First Setup

## Equipment used

* DJI M210 Drone
* ROCK R1A LiDAR payload
* EMLID Reach RS2 Survey kit
* 2m bi-pod
* Survey dual clamp tripod
* tribrach
* Maps Made Easy (Terrain Flight planning)(Still under Review)

## Attach the R1a to your vehicle

The R1a can be attached to any number of vehicles in order to acquire LiDAR data. In this quickstart we will assume you are attaching the LiDAR to a drone. If you are attaching to another vehicle please refer to our [Community](https://community.rockrobotic.com) for additional help.

Refer to the setup guide for your particular drone to connect the R1a.

* [DJI Matrice 300 RTK](../drone-setup/m300.md)
* [DJI Matrice 210](../drone-setup/m210.md)
* [DJI Matrice 600](../drone-setup/m600.md)

## Power on and Connecting to the R1a

First, ensure the supplied usb drive is inserted into the R1a. Then, power on the R1a. After powering up the unit, open Wi-Fi settings on your host computer (tablet, smartphone, or PC) and look for the wireless network labeled:

`ROCKrobotic-######`

Connect to this network using the following password:

`LidarAndINS`

Next, open up the web browser of your choice and go to the following web address:

`192.168.12.1`

<div style="text-align: center;"><img src="../img/web-interface.png" style="width: 450px;"></div>

## Configure the R1a

In order to obtain as accurate as possible LiDAR data from the R1a, the unit needs to be configured for the data acquisition vehicle. This includes the "IMU to Antenna Offset" and the "Vehicle to IMU Rotation". If using one of the provided setup kits, the information will be provided for you. If you are using another acquisition vehicle refer to the [Community](https://community.rockrobotic.com) for additional help.

## Setup your Base Station

A highly accurate trajectory is necessary for accurate results from the R1a. In order to obtain this accurate trajectory you must use a GNSS base station. We recommend the [Emlid Reach RS2](https://store.emlid.com/?ref=40). Follow the [RS2 documentation](https://docs.emlid.com/reachrs2/) for setting up your base station.

The base station should be configured to log Raw data in RINEX 3.03+ format for the entire duration of the R1a data acquisition.

## Calibrate the R1a

After turning on the R1a be sure to let the R1a sit in a static position for at least 5 seconds. Before turning on the LiDAR, you will need to fly a figure 8 pattern three times to ensure the IMU is calibrated. Once calibration is complete, land the drone.

## Collect Data

When you are ready to start collecting data click the 'Start' button within the web interface.

<div style="text-align: center;"><img src="../img/start.png" style="width: 300px;"></div>

The LiDAR, IMU, and GPS will all start collecting data. Proceed with your planned mission!

**Note:** To protect the user from accidently attempting to record data while the USB is unattached, the user does not have the ability to “Start” data recording in the “Status” window when the USB is unattached. When unattached the user will see the message shown below in Fig. 2-8. Message displayed when trying to record data while USB is unattached.

<div style="text-align: center;"><img src="../img/re-attach.png" style="width: 250px;"></div>

At the completion of the mission you will need to fly three additional figure 8 patterns with the drone and then land. Once on the ground let the drone sit for five minutes before stopping the data collection and powering off the unit.

Congratulations! You collected your first LiDAR data!

## Retrieve Data for Processing

All of the LiDAR, IMU, and GPS data is written to the usb stick which is attached to the R1a. When the unit is powered off you can detach the usb and insert into your PC to begin your processing.
