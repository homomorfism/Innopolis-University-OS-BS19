
#### Task 1

A process has been allocated 3 page frames and no pages of the process are initially available in the memory. The process references pages as follows: ```3, 5, 4, 6, 1, 3, 1, 4, 5, 3 ```

If Optimal page replacement algorithm is used, how many page faults will occur?

Select one:
- ```9```
- ```5```
- ```7```
- ```4```
- ```3```
- ```8```
- ```6``` <- **Correct**

> The optimal page replacement algorithm says that the page with the highest label should be removed. If one page will not be used for 8 million instructions and another page will not be used for 6 million instructions, removing the former pushes the page fault that will fetch it back as far into the future as possible. Computers, like people, try to put off unpleasant events for as long as they can.

Firstly, we have 3 page faults (to fill page frames), now in memory: ```3, 5, 4```.
Then, we want to add 6 (+1 page fault): page 3 will be referenced at 3-th access, page 5 - at 6-th access, page 4 - at 5-th access => so we drop page 5, now in memory: ```3, 6, 4```. And so on ;)

#### Task 2

A process has been allocated 3 page frames and no pages of the process are initially available in the memory. The process references pages as follows: 

```3, 5, 4, 6, 1, 3, 1, 4, 5, 3```

How many more page faults occur with FIFO than with the Optimal page replacement algorithm?

Select one:
- ```3```
- ```2``` <- **Correct**
- ```0```
- ```4```
- ```1```

#### Task 3


#### Task 4


#### Task 5


#### Task 6


#### Task 7


#### Task 8

Which of the following statements are **false**?

Select one or more:
- ```Small pages increase internal fragmentation``` <- **Bullshit**, small pages - more effective usage of space (pages are 50% filled approx.)
- ```Small pages help allocating space for multiphase programs with less memory wasted``` <- ```Idk really```
- ```Having many pages leads to a large page table``` <- Right, more pages - more entries in page table
- ```Transferring a small page takes significantly less time then transferring a large page``` <- **Not correct**
- ```Using small pages saves space in the TLB``` <- **Bullshit**, small pages - more entries, less address space could be stored in TLB


#### Task 9

A student has claimed that ‘‘in the abstract, the basic page replacement algorithms (FIFO, LRU, optimal) are identical except for the attribute used for selecting the page to be replaced’’. What is that attribute for the FIFO algorithm? LRU algorithm? Optimal algorithm? Select all that apply.
Select one or more:
- ```Nearest reference time in the future for Optimal``` <- **Correct**
- ```Nearest load time for Optimal```
- ```Page class for FIFO```
- ```Load time for FIFO``` <- **Correct**
- ```Amount of page frames for LRU```
- ```Latest reference time for LRU``` <- **Correct**
 
In FIFO we need to know time when page came (load time); in LRU we have a counter with time of last access, optimal algorithm - when in the future this page will be referenced.

#### Task 10




