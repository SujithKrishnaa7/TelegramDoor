ESP32-CAM Door Lock System with Telegram API
This project demonstrates how to use the ESP32-CAM module to control a door lock via a 5V solenoid. The system works by capturing an image when a push button is pressed and sending it to the admin via Telegram API for authentication. The admin can then decide whether to unlock or keep the door locked based on the image received.

Features
Captures image using ESP32-CAM when a visitor presses the button.
Sends the captured image to the admin via Telegram using the Telegram API.
Allows the admin to remotely unlock or lock the door using the Telegram interface.
Controls a 5V solenoid to lock or unlock the door.
Components Used
ESP32-CAM module
5V solenoid lock
Push button for triggering the camera
Jumper wires
Power supply (5V for the solenoid)
Telegram API for communication with the admin
Working
When the push button is pressed, the ESP32-CAM captures an image of the individual at the door.
The captured image is sent to the admin’s Telegram account via the Telegram Bot API.
The admin receives the image and can respond with either a command to unlock or keep the door locked.
Based on the admin’s response, the ESP32-CAM controls the 5V solenoid, either unlocking or keeping the door locked.
How to Use
Set up the Telegram Bot and obtain your Bot Token.
Flash the ESP32-CAM with the provided code.
Connect the ESP32-CAM, push button, and solenoid lock as per the circuit diagram (provided in the repository).
When someone presses the button, the ESP32-CAM will capture their image and send it to the admin via Telegram.
The admin can send a response through Telegram to either unlock or lock the door.
Circuit Diagram
(https://iotcircuithub.com/wp-content/uploads/2020/12/ESP32CAM-telegram-wifi-lock-circuit.jpg)]

Code
The code for this project can be found in the folder of this repository. 

ESP32-CAM setup for capturing images.
Integration with Telegram API for sending and receiving messages.
GPIO control for unlocking/locking the solenoid.
Libraries Required
ESP32-CAM library: for camera control.
WiFi library: to connect the ESP32-CAM to your home network.
UniversalTelegramBot library: to interact with Telegram API.
