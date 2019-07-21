# haunting-eye-2.0

PROJECT TITLE : HAUNTING EYE 2.0

DESCRIPTION:

OpenCV face tracking on the Raspberry Pi using Python. Controlling two servo motors to allow a Picam to pan/tilt while tracking a face in real time using Raspberry Pi.

#Step 1: Acquire the Hardware.

Things needed:

1.A raspberry pi2
2.A pan/tilt bracket -- I used a mini pan/tilt for servos 3D print
3.Two Servos
4.A GPIO Ribbon Cable
5.A Pi-Supported PiCam




Step 2: Get Your Raspberry Pi Ready


Make sure you are using the Official RaspbianOS (the hard-float version) and that it is up to date.
Install OpenCV for python3: sudo pip3 install python-opencv




Step 3: Put Together Your Rig

Build the pan/tilt brackets and attach the servos.
Attach your camera to the top of the bracket (I just used tape) and plug it into your raspberry pi.


Step 4: Connecting the Servos


servo-0 is connected to GPIO 4 and servo-1 is connected to GPIO-17.
Servos have three wires, one is red which is Vin/positive, one is brown or black which is ground/negative and the other is control.
using the ribbon cable (and in my case some connector wire jammed into the holes) connect the control wire for each servo to the correct pin. The code assumes that servo-0 will control the left-right movement and servo-1 will control the up-down movement of the camera; so connect them this way.

The Vin for the servos would come from the 5v pins from the GPIO and the ground for the servos would come from the ground pins of GPIO.

You will need some kind of external power source which is able to handle a heavy 5v-6v load:the servos are rated for up to 6v. The 5v pin on a computer power supply, a 5v-6v wall charger, some batteries in parallel; whatever floats your boat. Once you have your external source just connect the positive and negative lines from the servos to the positive and negative side of your power source, then connect the ground (negative) from your external power source to a ground pin on the raspberry pi GPIO.


Step 5: Run the Program

I have attached the python script to this article, it’s called Haunting_Eye2.0.py and PID.py to run it just CD to its location in terminal and type : python Haunting_Eye2.0.py 

