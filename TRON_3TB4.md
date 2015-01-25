TRON 3TB4 Summary
=================

* Instructor: Dr. Lawford 
* *Winter 2015*
* McMaster University
* *Primary Author*: Kemal Ahmed

-------------------------------

##CanBUS

**CanBUS**:

* 2-wire protocol: `CAN_H` and `CAN_L`  
* uses <ins>constructive arbitration</ins>
* When both lines have same voltage, signal is *recessive*
* If `CAN_H` - `CAN_L` > 0.9V, signal is *dominant*
* No ground reference, i.e. no ground noise
* Maximum transmission rate: 1 Megabit / s

**Dominant node**: zeroes

**Recessive node**: ones

**Ethernet** uses <ins>destructive conflict resolution</ins>.

**Prototols**: how to interpret/represent a set of inputs

**Slew Rate**: rate of change of voltage / s; how jagged are your square waves?

**Baud Rate**: number of signals; 1/period

RTR remote messages

**Arbitration**:

**Differential BUS**: when 2 wires travel along the same path, they experience the same external interference. To determine the message, you need to find the difference between the 2 wires, so you actually end up subtracting out the interference   

![CAN Data frame](images/can_data_frame.png)

Each CANBUS Node has:

* **Host processor**: generates messages to be sent; deciphers received messages
* **CAN Controller**: takes messages from host and transmits them to the bus
* **Transceiver**:

**Start Of Message (SOM) Bit**:

**Polling**: 

* **Normal mode**: 
* **Loopback mode**: sends TX from controller to RX; don't need acknowledgements
* **Silent mode**: sends RX to TX; more checking if messages are spam
* **Silent-loopback mode**: 

----

Message filtering:

* Software

**ElectroMagnetic Interference (EMI)**:

**