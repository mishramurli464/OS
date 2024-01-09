# OS
Operating System lies in the category of system software. It basically manages all the resources of the computer. An Operating System can be defined as an interface between user and hardware.  
It is responsible for the execution of all the processes, Resource Allocation, CPU management, File Management and many other tasks.  
![image](https://github.com/mishramurli464/OS/assets/128781536/ddccb556-f68a-448f-bb25-a2344288ca70)  

## Program  
Program is a static, or passive, entity stored in the disk. It is a file containing binary form of instructions.  
A program could store high-level programming language directly if that language is compiled at run time. Such program is called interpreted program.  

For example, we developers write code in high-level programming language such as C. Computer cannot read C directly so a compiler is in place to translate C into executable file, an exefile.  
This executable file is the Program. On the other hand, JavaScript and Python are interpreted program so we don’t have to compile it first.   

## Process 
Process is like an instance of a Program. When a program is loaded onto memory, it becomes Process and is now considered an active entity.  
Process requires more resources comparing to Program because when it is running, it needs memory and CPU to do the fetching and calculation.  
A program might associated with multiple process, and a process might includes multiple threads.  

## Thread
A thread is the basic unit of executable code in a process. It comes with its own set of registers and stack.  
A single-thread process means that a process could only perform a task one at a time. There is also multi-threads process, meaning it could run multiple tasks at a time.  
Of course multi-threads are more efficient, but it also brings some side effects that single thread wouldn’t encounter, such as deadlock and concurrency.  


## Multiprogramming vs Multiprocessing vs Multitasking vs Multithreading   

## Multiprogramming   
"The concurrent residency of more than one program in the main memory is referred as multiprogramming."  
Since multiple programs are resident in the memory, as soon as the currently executing program finishes its execution, the next program is dispatched for its consumption. 
Also if the currently executing program asks for input output resources then meanwhile another program is dispatched to the CPU for execution.  
The main objective of multiprogramming is:  
Maximum CPU utilization.
Efficient management of the main memory.

Multiprogramming can be virtually shown as:
![image](https://github.com/mishramurli464/OS/assets/128781536/eeeb067a-ab33-4972-880b-090ed636e7e5)  

##  Multiprocessing  
When one system is connected to more than one processor which collectively work for the completion of the task, it is called as multiprocessing systems.  
Multiprocessing systems can be divided in two types:  
Symmetric Multiprocessing: The operating system here resides on one processor and the other processors run user's programs.  
Asymmetric Multiprocessing: The OS runs on any available processor or all the processor simultaneously run the user program.  

Multiprocessing systems can be virtually represented as:  
![image](https://github.com/mishramurli464/OS/assets/128781536/a70df4b0-b368-42bc-a6f8-f58600d85011)  


## Multithreading  
"Multithreading is a conceptual programming paradigm where a process is divided into a number of sub-processes called as threads. Each thread is independent and  
has its own path of execution with enabled inter thread communication."  
"Thread is the path followed while executing a program. Each thread has its own program counter, stack and register."  
A thread is a light weight process.  

It can be virtually represented as:  
![image](https://github.com/mishramurli464/OS/assets/128781536/4fa0b580-9aa5-4d2d-9f35-13756ecba95e)  

## Multitasking  
Earlier when computers were invented, a user was allowed to submit only job or task at a time. But later with availability of high-speed processor, one can submit  
more than one task.  
So the capability of OS to accept more the one task per user is termed as multitasking.  
Multiple jobs are executed by the CPU simultaneously by switching between them.  
The various job can be accepted from same user or different users. There are 2 types of multitasking systems:  
Single User Multitasking  
Multi User multitasking  

It can be virtually represented as:  
![image](https://github.com/mishramurli464/OS/assets/128781536/4935604c-d00a-4e67-a518-7d0485181c38)  

## Process States  
The process, from its creation to completion, passes through various states. The minimum number of states is five.  

1. New  
A program which is going to be picked up by the OS into the main memory is called a new process.  

2. Ready  
The processes which are ready for the execution and reside in the main memory are called ready state processes. There can be many processes present in the ready state.  

3. Running  
One of the processes from the ready state will be chosen by the OS depending upon the scheduling algorithm. Hence, if we have only one CPU in our system, the number of
running processes for a particular time will always be one. If we have n processors in the system then we can have n processes running simultaneously.  

5. Block or wait  
From the Running state, a process can make the transition to the block or wait state depending upon the scheduling algorithm or the intrinsic behavior of the process.
When a process waits for a certain resource to be assigned or for the input from the user then the OS move this process to the block or wait state and assigns the CPU to
the other processes.  

5. Completion or termination  
When a process finishes its execution, it comes in the termination state. All the context of the process (Process Control Block) will also be deleted the process will
be terminated by the Operating system.  

7. Suspend ready  
A process in the ready state, which is moved to secondary memory from the main memory due to lack of the resources (mainly primary memory) is called in the suspend ready state  
If the main memory is full and a higher priority process comes for the execution then the OS have to make the room for the process in the main memory by throwing the lower  
priority process out into the secondary memory. The suspend ready processes remain in the secondary memory until the main memory gets available.   

7. Suspend wait   
Instead of removing the process from the ready queue, it's better to remove the blocked process which is waiting for some resources in the main memory. Since it is already
waiting for some resource to get available hence it is better if it waits in the secondary memory and make room for the higher priority process. These processes complete
their execution once the main memory gets available and their wait is finished.  











