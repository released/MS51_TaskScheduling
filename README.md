# MS51_TaskScheduling
 MS51_TaskScheduling

update @ 2020/01/08

platform : update MS51 driver to Keil_V1.00.003 , test in MS51 TSSOP20 EVM

1. using task (code base from internet) and array list , to control function and simply the procedure

2. current task max number , refer to define MAXTASKS

3. to add new function into task list

- add new function , task template refer to current task

- insert this new task into TaskList array , will automatically start the new task

4. to porting to other platform , 

- insert UpdateTimers() into TIMER interrupt IRQ with 1 ms

- calling TaskSchedulerInit() and TaskSchedulerStart() instead of while (1) after function init finish 