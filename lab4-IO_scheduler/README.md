# Operating-System-Lab4-IO scheduler
The lab4 for operating system. Implemented and simulated the scheduling and optimization of I/O operations. I provided many kinds of I/O schedulers.

The usage is 
`./ioshced -s<schedalgo> inputfile`

An example of usage is 
`./MMU -si input5`

The following scheduler algorithms are provided

FIFO: i
SSTF: j
LOOK: s
CLOOK: c
FLOOK: f

Different kinds of scheduler algorithms are implemented using the Object Oriented Programming. They all inherit from a super class IOsched. So the driver function simulation() has nothing to do with the type of the algorithms.
