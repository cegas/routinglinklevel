# Reliable link level routing algorithm over 802.15.4

This repository includes the source code for implementing a reliable link-level routing algorithm over a 802.15.4 physical layer especially designed for linear topologies (monitoring of pipeline infrastructures). The algorithm is described in the article "Reliable link level routing algorithm in pipeline monitoring using implicit acknowledgments" submitted to "Sensors". 


## Getting Started

Two files are provided:
* `codigo algoritmo nivel enlace.rar` provides the source code of the algorithm for RCB256RFR2 devices (an 802.15.4 node based on the single-chip ATmega256RFR2).
* `codigo medicion retardos.rar` provides code for measuring latency in the communications in different scenarios.


### Prerequisites
* Install Atmel Studio 7
* Download and decompress the files.
* A programmer is required to flash the code into the nodes (e.g. ATMEL ICE).  
* An 802.15.4 sniffer (e.g.Texas Instruments CS2531) can be useful for the development.


### Compiling

* Install the `Wireless Composer 7.0` extension (`Tools -> Extensions and Updates`) in your Atmel Studio 7 instance. 
* Import the project in `File -> Open -> Project` and select the "solution" `TRAMSMISOR_NOR_V16 - RS232 - CSMA - 19.atsln` (for the algorithm) or `ACK3.atsin` (for the additional tool to measure the communication latency). 
* Build the project with `Build Solutions`. This step will generate a `.hex` file to program the node. 

## Deployment

* Connect your programmer to the node (e.g. ATMEL ICE).
* Program the node with `Tools -> Device Programming`)
	+ In `Tool` select the programmer device (e.g ATMEL ICE). 
	+ Check that the voltage is at least 2.1 V.
	+ Ensure that the following options are enabled: 
		- `Erase device before programming`.
		- `Verify flash after programmin`.
		- `Verify EEPROM after programming`
	+ Flash the node with `Program` 

