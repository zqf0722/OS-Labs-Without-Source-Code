# Operating-System-Lab2-Scheduler
The lab2 for operating system. Implemented a process scheduler that takes the input details of multiple processes and schedule them. I provided many kinds of scheduler.

The usage is 
`./Scheduler [-p] [-s<schedulerspec>] inputfile randfile`

The scheduler specification is “–s [ FLS | R<num> | P<num>[:<maxprio>] | E<num>[:<maxprios>] ]”, where F=FCFS, L=LCFS,
S=SRTF and R10 and P10 are RR and PRIO with quantum 10. (e.g. “./sched –sR10”) and E10 is the preemptive prio scheduler.

FCFS stands for first-come-first-served
LCFS stands for last-come-first-served
SRTF stands for shortes-remaining-time-first
RR stands for round-robin
PRIO stands for priority 

Supporting this parameter is required and the quantum is a positive number. In addition the number of priority levels is specified in PRIO and PREPRIO with an optional “:num” addition. E.g. “-sE10:5” implies quantum=10 and numprios=5. If the addition is omitted then maxprios=4 by default.

-p only has meaning when the scheduler type is Preemptive Priority Scheduler. It shows the decision for every possible preemption.

Different kinds of scheduler are implemented using the Object Oriented Programming. They all inherit from a super class scheduler. So the driver function simulation() has nothing to do with the type of the scheduler.
