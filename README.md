# BlueBox
Project Working Title: BlueBox 

// 18-05-16
Step One: Try collecting data from the Bluetooth Module 
Bluetooth Module: Sparkfun Smirf Gold 
Cost: A$ 23.80 www.element14.com.au

          ----xxx----
The idea is to change the initial sketch to reflect the following changes:
1. Data is acquired from the sensors by the arduino. Bluetooth on the indiviadual data acquisition nodes is in the "Slave" mode.
2. The data is then (somehow??) encoded into 248 byte i.e. the length of the User Defined bluetooth name.
3. The bluetooth "command mode" is entered and the device name is changed to the output value of Step 2
4. The signal of the "Slave" device is then picked up by the "Master" Bluetooth Module. 
5. This  has 3 parts I. The bluettooth mac address/name: This identifies the device and Data Acquisition node
                    II. The User Defined 248 byte long Bluetooth name: This transmits the sensor signal to the "Master" device without       essentially connecting to it. 
                    III. A Hexadecimal Value signifying the signal strength: Signal strength is inversley proportional to the distance        from the "Master" device. 
          ----xxx----

Further on: The Master device then transmits this information over the internet (Wifi?) to a cloud server.
            The server logs the values and simplifies the data into readable values.
            It then feeds these values into an artificial neural network which corealates the data set values from the sensors with other data sets available into a learning algorithm 
            This raw data and stored historical data values are pulled off the cloud server by a web app that simplifies the data into graphs and charts. 
            
Things to do:
System Structure Diagram 
Data Flow Diagram
Contextual Diagram 

