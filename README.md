# Control-Robot-Movement-Using-Interface-Panel
Design an interface to control the movement of the robot which could be (forward, left, backward, right, stop)

Design an interface to control the movement of the robot which could be in (forward, left, backward, right) direction. When user click on a certain direction the movement will be stored in a database

![1](https://github.com/ya77ya/Control-Robot-Movement-Using-Interface-Panel/assets/90250848/2c5afb7c-9e02-429b-9644-107bcb7ee800)


## Pre-requisites
 To be able to send and get data from the MYSQL database we have to install MYSQL database, you can use [XAMPP](https://www.apachefriends.org/) which I an open-source cross-platform web server
 
 ![screen2](https://github.com/ya77ya/Control-Robot-Movement-Using-Interface-Panel/assets/90250848/f86eab8d-f942-47b4-9f56-5852c7c035c5)

 
 ## Explanation Steps
 1. After installing XAMPP create a folder named "movement" in xampp path *xampp>htdocs*
 
 2. Copy the two files attached above, sendMovementValues, and getMovement.php to the "movement" folder
 

4. Before uploading the code **Movement.ino** , make sure to change the **ssid** and **password** to your WiFi. After uploading the code will read the data from the database frequently using GET method

5. In **phpMyAdmin**, create a database named "esp32", then create a table named "movement" with values shown in the below image

![screen3](https://github.com/ya77ya/Control-Robot-Movement-Using-Interface-Panel/assets/90250848/f2701a1d-479f-4c60-ac29-eaa63f787b56)


6. When the user clicks the forward button, the page of website will send "forward" to the database and ESP32 will read it to move forward, and when the user clicks the right button, we will send "right" to the database and ESP32 will also turn right

As you see in the image above, we also register how long the user pressed the button, he clicked the forward button for 3.3 seconds and clicked the right button for 1.6 seconds. This is useful later if we want the robot to replay what the user clicked before


