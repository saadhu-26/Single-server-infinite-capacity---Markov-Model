# Single server with infinite capacity (M/M/1):(oo/FIFO)

## Aim :
To find (a) average number of materials in the system (b) average number of materials in the conveyor (c) waiting time of each material in the system (d) waiting time of each material in the conveyor, if the arrival  of materials follow poisson process with the mean interval time 12 seconds, serivice time of lathe machine follows exponential distribution with mean serice time 1 second and average service time of robot is 7seconds.

## Software required :
Visual components and Python

## Theory:
Queuing are the most frequently encountered problems in everyday life. For example, queue at a cafeteria, library, bank, etc. Common to all of these cases are the arrivals of objects requiring service and the attendant delays when the service mechanism is busy. Waiting lines cannot be eliminated completely, but suitable techniques can be used to reduce the waiting time of an object in the system. A long waiting line may result in loss of customers to an organization. Waiting time can be reduced by providing additional service facilities, but it may result in an increase in the idle time of the service mechanism.

![image](1.png)

This is a queuing model in which the arrival is Marcovian and departure distribution is also Marcovian,number of server is one and size of the queue is also Marcovian,no.of server is one and size of the queue is infinite and service discipline is 1st come 1st serve(FCFS) and the calling source is also finite.

## Procedure :

![imAGE](2.png)

## Experiment:

<img width="759" height="434" alt="Screenshot 2026-05-25 194635" src="https://github.com/user-attachments/assets/9ccb38f0-8857-4fd6-bb5d-33846f1591a5" />

## Program :
```
arr_time=float(input("Enterthe meaninterarrival timeof objects fromFeeder(insecs):"))
ser_time=float(input("Enterthe mean interservicetimeof LatheMachine(insecs): "))
Robot_time=float(input("EntertheAdditional timetakenfor theRobot(insecs): "))
lam=1/arr_time
mu=1/(ser_time+Robot_time)
print("--------------------------------------------------------------")
print("SingleServerwithInfiniteCapacity-(M/M/1):(oo/FIFO)")
print("--------------------------------------------------------------")
print("Themeanarrival rateper second: %0.2f"%lam)
print("Themeanservice rateper second: %0.2f"%mu)
if(lam< mu):
Ls=lam/(mu-lam)
Lq=Ls-lam/mu
Ws=Ls/lam
Wq=Lq/lam
print("Averagenumberofobjects inthe system :%0.2f"%Ls)
print("Averagenumberofobjects inthe conveyor: %0.2f"%Lq)
print("Averagewaiting timeofan object inthesystem: %0.2f secs"%Ws)
print("Averagewaiting timeofan object intheconveyor :%0.2fsecs"%Wq)
print("Probability thatthe system isbusy: %0.2f"%(lam/mu) )
print("Probability thatthe system isempty: %0.2f"%(1-lam/mu))
else:
print("Warning!ObjectsOver flowwillhappenintheconveyor")
print("---------------------------------------------------------------")
```
## Output :

<img width="757" height="289" alt="Screenshot 2026-05-25 194800" src="https://github.com/user-attachments/assets/e44b74a5-d65b-4609-90aa-4e0904d609ff" />

## Result :

Thus, the program has been executed successfully and the required parameters have been calculated as per the given
conditions.
