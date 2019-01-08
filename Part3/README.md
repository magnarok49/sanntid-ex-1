# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > *Concurrency, at software design level is where several tasks can be in progress simultaneously.*
 > *Parallelism, at a run-time level, is where several instructions can be executed at once.*
 
 ### Why have machines become increasingly multicore in the past decade?
 > *More parallelized software, easier performance boost than increasing clock speed.*
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > *Several independent tasks running at the same time, that all require (some) execution, but not the full execution time of the core.*
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > *Both for sure, independent things are good for concurrency, dependent things can become a mess if not handled properly.*
 > *On a plus side, things definitely become more structured (code quality wahei)*
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > *Threads are separate "branches" within the same program, and usually share memory space.*
 > *Thus several threads can exist within a process.*
 > *Green threads are handled by a runtime or a vm (hypervisor) rather than the OS.*
 > *Coroutines are bits of code that run from start to finish, one at the time. They can seize to run other coroutines, then resume from where they seized.* 
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > *Threads*
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > *It limits multiple threads from accessing the same memory simultaneously, although only for 100 atomic operations.*
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > *Using the multiprocessing module in python.*
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > *How many threads are allowed to run at a single time. Thus limiting this to 1 ensures that a single thread is able to do its job without other threads interfering.*
