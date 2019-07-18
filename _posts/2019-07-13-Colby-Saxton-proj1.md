---
layout: post
title: "Lampi: Internet of Things Lamp"
date: 2019-05-4
---

The Project
-----------
This project was centered around building a fully functional IoT connected Lamp with a Touchscreen, Pub/Sub connectivity protocol, Web application, Mobile application and Facial Recognition Login. The Lampi is powered by a Raspberry Pi 3 Model B+ running Rasbian Stretch Lite. The lampi has LED lights that are controlled using the pigpio library.

The project uses SSH to log in to my Pi and to log in to my Amazon Web Services EC2 instance.

This project uses ansible as a method to install the professor's correct solution to weekly assignments.

This Lamp was made in a course at CWRU called Introduction to Connected Devices.



Touchscreen
-----------
This lamp uses a PiFTF 2.8" capacitive touchscreen.

Additionally, it uses Kivy as the UI. The UI has 3 sliders for controlling the hue, saturation and brightness and then an on-off button.

Here is a demonstration:
<video width="720" height="440" controls="controls">
  <source src="/../TouchscreenDemo.mp4"/>
</video>



Sub/Sub Connectivity protocol
-----------------------------
This lamp uses a pub/sub communication model where it can publish and subscribe to certain topics within a centralized broker.

This uses libraries called MQTT, Python Paho, JSON messages, and MQTT-Daemon within an Amazon EC2 instance to achieve this framework. This allows multiple lamps to be connected to the same broker.



Web Application
---------------
The Web Application made uses an NGINX/uWSGI web server to run off my Amazon EC2 instance. Additionally, Paho JS and JSON files was used to communication messages between the website and any connected lamps.

The web app uses a Django framework as well as an SQLite database to serve requests and dynamically update the web app.

Here is a demonstration of the web application:
<video width="720" height="440" controls="controls">
  <source src="/../WebAppDemo.mp4"/>
</video>



iOS Application
---------------
The iOS application was developed in XCode using Swift and Bluetooth Low Energy to connect and control the lamp from an iOS device.

Here is a demonstration:
<video width="720" height="440" controls="controls">
  <source src="/../iPhoneDemo.mp4"/>
</video>



Facial Recognition Login
------------------------
For the final project for this course, I decided to make a facial recognition login feature on the lamp. This login uses openCV, Pi-Face-Recognition and Kivy libraries. Additionally, I used a PiCamera and the PiCamera library to take images of a user attempting to login. Then I send the images to the backend where it is compared to a model trained to my face.

When I am not logged in, a message prevents me from using the lamp, however after logging in, the lamp becomes usable.

Here is a demonstration (be patient while it logs in!):
<video width="720" height="440" controls="controls">
  <source src="/../FaceRecognitionDemo.mp4"/>
</video>
