# node-red-contrib-crobfaces
A <a href="http://nodered.org" target="_new">Node-RED</a> node to extract faces from a photo on a Raspberry Pi. This node will only work on an Raspberry Pi with <a href="http://opencv.org" target="_new">OpenCV</a> Framework installed. 


Install
-------

Run the following command in the root directory of your Node-RED install or home directory (usually ~/.node-red) and will also install needed libraries.

        npm install node-red-contrib-crobfaces

### Additionally you have to install on the Raspberry Pi 

The detect node also utilizes the <b>OpenCV Framework</b> to give some additional capabilities to the photo processing (detect faces). Therefore you have to install it on your Raspberry Pi. 
Take a look at this <a href="http://www.pyimagesearch.com/2015/07/27/installing-opencv-3-0-for-both-python-2-7-and-python-3-on-your-raspberry-pi-2/" target="_new">tutorial</a> to see how to install.

This node is an extension to the node-red-contrib-camerapi - which helps you to take photos with the installed Raspberry Pi Cam. 

Usage
-----

Provides a node to capture faces.

### DetectFaces

If you choose the Face-Detection (based on OpenCV Framework) - you will also get in msg.facescount the number of detected faces and a JSON with the necessary information to the detected face (x,y,x+w,y+h) and if in filemode the name, path and format of the file with the face cut from the image. 