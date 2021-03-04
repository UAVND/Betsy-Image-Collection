# Image Collection Using Betsy

## General Idea

Utilize *ROS* Noetic for the creation of a image collection package that will be run onboard Betsy (V1 fixed wing prototype) via a companion computer. The companion computer will most likely be a Raspberry Pi 4 with 8GB of RAM. The camera will interface with the flight controller (Pixhawk Cube) via a PWM to analog converter cable. The camera will most likely be a Canon Powershot. The *LUA* scripts loaded on the camera's SD card will be uploaded shortly. 

## Project Context

The UAVND vehicle for the AUVSI SUAS competition will require an alphanumeric recognition system. The competition task involves the detection, classification, and localization of alphanumeric symbols scattered around the competition grid. An example of such a symbol is portrayed below. 

![This is an example of an alphanumeric symbol](https://github.com/UAVND/Betsy-Image-Collection/blob/master/images/AlphanumericExample.jpg?raw=true)

In order to create a system capable of the aforementioned task, we will need to possess a substantial training set of images to train our model. These images will need to be taken from the expected cruise altitude of the vehicle and other lower altitudes which may be encountered if an image which cannot be resolved from the cruise altitude. At the moment,  the cruise altitude is set be 250 feet. That being said, we need to have a tool for collecting these images. Training sets can be bought online. 

However, in most cases, they are prohibitively expensive. This is significant due to the fact that we are on a tight budget this year. Having a tool for the collection of these images using Betsy would be immensely useful. We would like to have the ability to go out to a field, lay out some of these symbols on the ground, input their presumed locations into this program, and have the vehicle go out and collect images from various angles and altitudes. After having depleted its battery or collected all the images needed, the vehicle needs to return and land successfully at its home location. 

## First Step 
The first step in this project will be familiarizing yourself with *MAVROS* and the functionality that it provides. *ROS* and *MAVROS* in particular comprise crucial pieces of our system. 

On your own branch, construct a node (or set of nodes) that utilize the topics and services provided by the *MAVROS* node to have the drone fly a zig-zag trajectory between two specified waypoints. It should be possible to modify the number of zig-zags and their width. 

Make sure to test extensively in a simulator seeing that we will be testing your program out on the field sometime in the next few weeks. 



