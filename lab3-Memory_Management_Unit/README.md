# Operating-System-Lab3-Memory Management Unit
The lab3 for operating system. Implemented a memory management unit that maps the virtual address spaces of multiple processes onto physical frames using page table translation. I provided many kinds of page replacement algorithms.

The usage is 
`./MMU -f<num_frames> -a<algorithms> [-o<options>] inputfile randfile`

An example of usage is 
`./MMU -f4 -ac -oOPFS in11 rfile`

The following options are supported

The ‘O’ option shall generate the required output

The ‘P’ (pagetable option) should print after the execution of all instructions the state of the pagetable

The ‘F’ (frame table option) should print after the execution and should show which frame is mapped at the end to
which <pid:virtual page> or ‘*’ if not currently mapped by any virtual page

The ‘S’ option prints per process statistics “PROC[i]” and the summary line (“TOTALCOST …”)

The ‘a’ option prints additional “aging” information during victim_selection and after each instruction for complex
algorithms 

The following page selection algorithms are provided

FIFO: f
Random: r
Clock: c
Enhanced Second Change: E
Aging: a
Working Set: w

Different kinds of page selection algorithms are implemented using the Object Oriented Programming. They all inherit from a super class MMU. So the driver function simulation() has nothing to do with the type of the algorithms.
