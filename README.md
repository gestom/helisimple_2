Helisimple
============

This simple app reads image from the AR Drone 2.0 and displays it on the screen.
If you click an object with distinct color, it will start to search for a largest object of that color in the image.
Pressing R makes the app forget the tracked color.

####CONTROLING
Q and A are takeoff and land, keypad numbers move the drone.
Z,X changes a camera.
Pressing ENTER saves current image. 

If you have a joystick, buttons 7 and 5 takeoff and land, buttons 1-4 switch cameras.
Axes 0-3 change angles and height.
The code is commented inside, start with main/heli.cpp so see how it works. 

#####COMPILING
Just type ''make'' in the src directory.
The soft needs standard libraries, SDL-devel lib for GUI and ffmpeg (libavutil,libavcodec,libswscale,libz) for video processing.

######ISSUES
Make sure your firewall accepts UDP and TCP connections on relevant ports - i.e. 5557 for UDP and 5555 for TPC.
The image bottom 8 rows part are incorrectly decoded - I have left them out for now.
A simple application that allows drone control by a keyboard or a joystick, acquires drone sensory data and performs a simple image analysis.
