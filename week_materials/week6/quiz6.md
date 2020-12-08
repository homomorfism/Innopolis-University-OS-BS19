#### Task 1

A set of operations that can be combined so that they appear to the rest of the system to be a single operation is called:
Select one:
- ```Mutual exclusion```
- ```Bounded buffer```
- ```Atomic operation``` <- **Correct**
- ```Critical region```
- ```Race conditions```

#### Task 2

Producer sleeps until awakened by consumer when buffer is NOT full; Consumer sleeps until awakened by Producer when buffer is NOT empty. This is:
Select one:
- ```Atomic operation```
- ```Solution to the bounded buffer problem ``` <- **Correct**
- ```Bounded buffer problem```
- ```Race condition```
- ```Priority inversion```

Sleep & wake locks are a way for avoiding race condition 

#### Task 3

The situation when a higher priority process has to wait for a lower priority process is called:
Select one:
- ```Bounded buffer problem```
- ```InterProces communication```
- ```Priority inversion ``` <- **Correct**
- ```Atomic operation```
- ```Race condition```

Logically, no other choices suits.

#### Task 4

The situation when a process is continuously testing a variable until some value appears is called:

Select one:
- ```Strict alternation```
- ```Priority inversion```
- ```Atomic operation``` 
- ```Busy waiting``` <- **Correct**, obviously

#### Task 5

Consider the 2-process solution to the critical section (‘i’ refers to the current process and ‘j’ is the other one): 

(as in slides on lecture 5 we consider flag and turn to be shared)


Process 1
```
repeat
     flag[i]:=true;
     turn := j;
     while ( flag[j] and turn ==j ) do no-op;
     <critical section>
     flag[i] := false;
     <remainder section>
 until false;
```

Process 2
```
repeat
     flag[j]:=true;
     turn := i;
     while ( flag[i] and turn ==i ) do no-op;
     <critical section>
     flag[j] := false;
     <remainder section>
 until false;
```

This solution satisfies:

Select one:
- ```Mutual Exclusion``` 
- ```Bounded Wait (no process should have to wait forever to enter into critical section)``` 
- ```Progress (process should eventually be able to complete)```
- ```All of the above ``` <- **Correct**

This is the Peterson solution, it satisfy all conditions of critical region. 
(Please write more understandable explanation to it).

#### Task 6

Which of the following are necessary to create a working solution to avoid race conditions?

Select one or more:
- ```All the processes must have different priorities```
- ```No process should enter its critical region inside a loop```
- ```No two processes may be simultaneously inside their critical regions ``` <- **Correct**
- ```No process running outside its critical region may block any process``` <- **Correct**
- ```More than one instance of any program should not be allowed to run simultaneously```
- ```No process should have to wait forever to enter its critical region ``` <- **Correct**

> Although this requirement avoids race conditions, it is not sufficient for having
parallel processes cooperate correctly and efficiently using shared data. We need
four conditions to hold to have a good solution:
>- No two processes may be simultaneously inside their critical regions.
>- No assumptions may be made about speeds or the number of CPUs.
>- No process running outside its critical region may block any process.
>- No process should have to wait forever to enter its critical region.

Tanenbaum, 120 page.

#### Task 7

#### Task 8

#### Task 9


#### Task 10