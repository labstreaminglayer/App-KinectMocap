# Kinect Mocap App for LSL

## Overview

The program connects to the first Kinect on your computer and streams the joint positions (as well as some extra data) of up to two tracked persons. For details, take a look at the channel labels and properties associated with the stream.

Check the Releases page for a compatible download, otherwise you will have to [build it yourself](#develop-and-build).

## Usage

This program requires the Kinect Runtime 1.8 to be installed: https://www.microsoft.com/en-us/download/details.aspx?id=40277

  * Make sure that your Kinect is powered on, connected to your computer and that it has fully booted, which might take a few seconds (there is a green LED on the front).

  * Start the KinectMocap app. This is a console program which has no GUI. The app will close itself when no Kinect was found; otherwise it will automatically link itself to the LSL and start streaming data.

  * The Kinect will automatically assign a tracking ID to any person walking into the picture (at a supported distance) and return position and confidence values for that person's joints. The joints (and correspondingly the channels) are anatomically labeled as in the following picture:

> ![http://i.msdn.microsoft.com/dynimg/IC534688.png](http://i.msdn.microsoft.com/dynimg/IC534688.png)

  * To consistently track with multiple people crossing the sensor view  it is important to use the tracking id to identify position data consistently with a person. Do not rely on the order of the channels for this purpose if you are tracking multiple users.

## Develop and Build

Download and install the Kinect for Windows SDK 1.8 from here: https://www.microsoft.com/en-ca/download/details.aspx?id=40278

