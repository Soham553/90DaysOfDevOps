Process in the linux based operationg system is an instance of a program or command.
There are 5 states a process can go through. The following are the 5 states
1. Running or Runnable (R):
   A command or a program is running when it is in the starting phase. Due to multitasking, when cpu can not be distributed equally, the program goes in runnable state
2. sleeping: Uninterruptible (D) and Interruptible (S)
    When the program is waiting for resources, it goes in uinterruptible state in which it will not respond to any signal.
    The program is waiting for input, then it will go in interruptible state
3. Stopped State (T):
     From a running or runnable state, we could put a process into the stopped state (T) using the SIGSTOP or SIGTSTP signals.
5. Zombie State (Z):
      When a process has completed its execution or is terminated, it’ll send the SIGCHLD signal to the parent process and go into the zombie state.













List 5 commands you would use daily
Keep it short and practical (under 1 page)
Use bullet points and short headings
