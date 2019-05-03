**1. List all of the main states a process may be in at any point in time on a standard Unix system. Briefly explain what each of these states means.**

New(Create) -- A process is about to be created but not yet created

Ready -- After creation of a process, the process enters the ready state, the process is loaded into the main memory, and waiting to get the CPU time for its execution.

Run -- The process is chosen by CPU for execution and the instructions within the process are executed by any one of the available CPU cores.

Wait -- Whenever the process requests access to I/O or needs an input from the users or needs access to a critical region it enters the blocked or wait state. Once the I/O operation is completed the process goes to ready state.

Terminated -- A process is killed as well as PCB is deleted.

**2. What is a zombie process?**

If the parent decides not to wait for the child’s termination and it executes its subsequent task, then at the termination of the child, the exit status is not read. Hence, there remains an entry in the process table even after the termination of the child. This state of the child process is known as the Zombie state.

**3. How does a zombie process get created? How does one get destroyed?**

Zombie processes usually occur for child processes, as the parent process still needs to read its child’s exit status. Once this is done using the wait system call, the zombie process is eliminated from the process table.

**4. What are some of the benefits of working in a compiled language versus a non-compiled language? More specifically, what benefits are there to be had from taking the extra time to compile our code?**

A compiled language is one where the program, once compiled, is expressed in the instructions of the target machine.

-- Faster performance by directly using the native code of the target machine
-- Opportunity to apply quite powerful optimisations during the compile stage

A non-compiled language is one where the instructions are not directly executed by the target machine, but instead read and executed by some other program (which normally is written in the language of the native machine).
-- Easier to implement
-- No need to run a compilation stage: can execute code directly "on the fly"
