# Robotics

Resources: 

Processing, https://processing.org/. To have a deeper look in how to use processing to create the GUI. 

Zumo32U4 example code such as the line follower, proximity and line sensors and motor code. 

Arduino website, https://www.arduino.cc/. To enhance my understanding of the code and using the Arduino IDE. 

Zumo website, https://www.pololu.com/product/2509. To understand how the Zumo works such as where the sensors are located. 

 

Mode 1 

For mode 1 first I started by looking at the motors example to understand how the motors worked once I got the motors to work, I had a look at the robot arm sketch and used similar case statements to move the motors depending on the character pressed. I had a look at the Arduino examples from week 1 and week 2 to remind me how to write to the serial monitor. Also had a look at the line sensor examples and the buzzer example so that it would buzz if it was at an edge. 

 

Mode 2 

 

For Mode 2 I built upon mode 1 and incorporated proximity sensors so that it could detect an object and implemented different if statements for different scenarios such as object or corner detected. Originally, I started off by just using proximity sensors but once I realised that these would not detect the black tape, I switched to using line sensors for the edges and proximity sensors for the object. I changed from the first draft where it only detected an object and sent a message back to where it detected the object and reacted accordingly to avoid it and attempted to implement a vector to hold directions so that they can be used to determine the location of the object such as take a left and then a right and also be used to get back to base by retracing the steps by iterating through the vector. 

For the final iteration of mode 2 I removed the code for manually moving the Zumo from the if statements and instead placed it in a function appropriately named manual mode to condense and refine the code by reducing repetition and so that the function can be called whenever needed. I also discovered that the vector code did not work so I decided to remove it. I removed some other code realising that it needs to be manually done instead of automatically such as when encountering an end of a corridor and implemented a few more cases in the manual mode switch statement such as turning a full 180o when the end of a corridor. Once the manual mode is complete it prints a statement letting the user know that it is switching back to automatic mode. 

Another difference between mode 1 and 2 is that I removed the buzzer so that when encountering the edge, it moves away instead of making a noise. 

 

Mode 3 

 

Built upon mode 2 but making it fully automatic by reversing away and then turning left or right. Implemented if statements within the if statements that senses that it is in a corner so that the Zumo once realising it is in a corner and checks if it is better to move towards the left or right. 

In the final iteration condensed and further optimised and refined the code as I realised that I did not need a separate if statement to check the direction of turning as if it was on the left corner turn right and if it is in a corner to the right turn left. 

 

GUI 

Implemented keyboard presses so now we can control the Zumo without a serial monitor or by pressing buttons. 

 

To start 

Upload the appropriate mode which you want to test to the Zumo, then run the Gui after closing the Arduino code. 

For mode 1 you just need to either press the buttons or the appropriate keyboard presses. 

For mode 2 it is like mode 1, however you may need to press e to begin as the Zumo may be stuck in manual mode. 

Mode 3 the Zumo should automatically start without user interaction 

1) Clone the repository 

2) Open folder named Final. 

3) Open the mode you want to test, example – Mode 1 then upload it to the Zumo via USB cable. 

4) Close the Arduino IDE. 

5) Open the Processing files and run it. 

 
