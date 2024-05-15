# CPU Schedulers Simulator

# Description:
## 1. Non-Preemptive Shortest- Job First (SJF) (using context switching)
## 2. Shortest- Remaining Time First (SRTF) Scheduling (with the solving of starvation problem using any way can be executed correctly)
## 3. Non-preemptive Priority Scheduling (with the solving of starvation problem using any way can be executed correctly)
## 4. AG Scheduling :
### a. The Round Robin (RR) CPU scheduling algorithm is a fair scheduling algorithm that gives equal time quantum to all processes So All processes are provided a static time to execute called quantum.
### b. A new factor is suggested to attach with each submitted process in our AG scheduling algorithm. This factor sums the effects of all three basic factors ((random_function(0,20) or 10 or priority), arrival time and burst time)The equation summarizes this relation is: AG-Factor = (Priority or 10 or (random_function (0,20)) + Arrival Time + Burst Time
### c. A new Random function (RF) is suggested between (0,20) and attached with each submitted process in our AG scheduling algorithm. This RF can update the AG- Factor based on the random number,
####  If(RF()<10 )-> AG-Factor = RF() + Arrival Time + Burst Time
####  If(RF()>10 )-> AG-Factor = 10 + Arrival Time + Burst Time
####  If(RF()=10 )-> AG-Factor = Priority + Arrival Time + Burst Time
### d. Once a process is executed for given time period, it’s called Non-preemptive AG till the finishing of (ceil (50%)) of its Quantum time, after that it’s converted to preemptive AG
####  preemptive AG : processes will always run until they complete or a new process is added that requires a smaller AG-Factor
### e. We have 3 scenarios of the running process:
#### i. The running process used all its quantum time and it still have job to do (add this process to the end of the queue, then increases its Quantum time by (ceil(10% of the (mean of Quantum))) ).
#### ii. The running process didn’t use all its quantum time based on another process converted from ready to running (add this process to the end of the queue, and then increase its Quantum time by the remaining unused Quantum time of this process).
#### iii. The running process finished its job (set its quantum time to zero and remove it from ready queue and add it to the die list).

# Program Input:
###  Number of processes
###  Round Robin Time Quantum
###  context switching
## For Each Process you need to receive the following parameters from the user:
###  Process Name
###  Process Color(Graphical Representation)
###  Process Arrival Time
###  Process Burst Time
###  Process Priority Number

# Program Output:
## For each scheduler output the following:   
###  Processes execution order
###  Waiting Time for each process
###  Turnaround Time for each process
###  Average Waiting Time
###  Process Color(Graphical Representation)
###  Print all history update of quantum time for each process (AG Scheduling)
###  Process Burst Time
###  Process Priority Number 