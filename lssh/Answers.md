
1. List all of the main states a process may be in at any point in time on a standard Unix system. Briefly explain what each of these states mean.
    * Ready/Waiting: The process is inside a queue within the main memory, waiting to be exectued by a CPU.
    * Running: The process has been chosen for execution, and its instructions are carried out by a CPU.
    * Blocked: The process requires something outside of itself, such as user input or a response from hardware, in order to continue being exectued.
    * Terminated: The process has either been completed or explicitly halted. Once its status/response has been read, it is removed from the queue.

2. What is a Zombie Process? How does it get created? How does it get destroyed?
    * A process will become a zombie process when it is terminated/finished, meaning it has either completed its purpose or been halted. Either way, it will wait for its exit status to be read (usually by a parent process). Once this happens, it will be destroyed/removed from memory. A zombie process is only dangerous if the parent process is not set up correctly to read its exit status, in which it sticks around in memory and hogs its process ID.

3. Describe the job of the Scheduler in the OS in general.
    * In modern computers, multiple processes can be available to run at any given time. Thus, it is the job of the Scheduler to determine which process should be exectued next, with the main goals of maximizing efficiency, a positive user experience, and fairness between processes.

4. Describe the benefits of the MLFQ over a plain Round-Robin scheduler.
    * A round-robin scheduler prioritizes equal execution time among processes, but a multi-level feedback queue realizes that not all processes are equally important. A MLFQ scheduler determines priority levels as it goes through the process queues, resulting in a more-optimized turnaround time, a more flexible scheduler, and a reduction in response time.
