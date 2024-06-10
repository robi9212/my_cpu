# my_cpu
## cpu_simulator

This CPU simulator is able to fetch and parse instructions 

Fetch and parse initial values from memory to seperate input files

Send CPU unstructions and inital memory bus values to CPU and memory bus

there is output for user documenting stages of input processing

Implemented ISA that can handle MIPS Instructions such as the following:

Instruction	    Operand	        Meaning
ADD	            Rd, Rs, Rt	    Rd <- Rs + Rt;
ADDI	        Rt, Rs, immd	Rt <- Rs + immd
SUB	            Rd, Rs, Rt	    Rd <- Rs - Rt
SLT	            Rd, Rs, Rt	    If (Rs < Rt) then Rd <- 1 else Rd <- 0
BNE	            Rs, Rt,         offset	If (Rs not equal Rt) then PC <- (PC + 4) + offset * 4
J	            target	        PC <- target * 4
JAL	            target	        R7 <- PC + 4; PC <- target *4
LW	            Rt, offset(Rs)	Rt <- MEM[Rs + offset]
SW	            Rt, offset(Rs)	MEM[Rs + offset] <- Rt
CACHE	        Code	        Code = 0(Cache off) Code = 1(Cache on), Code = 2(Flush cache)
HALT	        ;	            Terminate Execution

