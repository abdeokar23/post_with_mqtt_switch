# Posting data to a Blockchain using NodeMCU

This code deals with POSTing sensor data to a blockchain. The sensor used in this example is a DHT11, and the data being POSTed to the blockchain is temperature. 

We use the ArduinoJson package to bundle the data that we send to the blockchain. The POSTing of the data is controlled by an MQTT switch based off of Adafruit MQTT dashoard control. The examples of creation of a switch on io.adafruit are available online. or can be found as a subsection in the following repo:

Network Time Protocol(NTP) library is being used to get a time stamp to associate the sensor data fetched with the particular time it was fetched at. NTP offset needs to be adjusted according to the particular time-zone you desire.

The reader() was defined to state value of the Adafruit MQTT feed. The snippet will ascertain the ON state and allow the loop() to start posting sensor data on the blockchain.