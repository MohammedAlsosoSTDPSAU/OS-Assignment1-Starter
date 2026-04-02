# Development Log

## Instructions
Document your development process as you work on the assignment. Add entries showing:
- What you worked on
- Problems you encountered
- How you solved them
- Time spent

**Requirements**: Minimum 5 entries showing progression over time.

---

## Example Entry Format:

### Entry 1 - [April 1, 2026, 2:30 PM]
**What I did**: Forked the repository and set up my student ID

**Details**: 
- Created GitHub account with university email
- Forked the starter repository
- Changed student ID on line 92 to my actual ID (441234567)
- Compiled and ran the program successfully

**Challenges**: Had to install JDK first because javac wasn't recognized

**Solution**: Downloaded JDK 17 from Oracle website and set PATH variable

**Time spent**: 30 minutes

---

## Your Development Log:

### Entry 1 - [March 20, 2026]
**What I did**: Setting up the  GitHub repository and local enviromnent.

**Details**: Forked the starter repository OS-Assignment1-Starter to my personal GitHub account. Cloned the repo locally and updated line 92 in SchedulerSimulation.java with my unique Student ID to initialize the random seed.

**Challenges**: Connecting VS Code to my GitHub account using the university email.

**Solution**: Followed the VS Code GitHub integration tutorial and verified my university email.

**Time spent**: 1 hour. 

---

### Entry 2 - [March 22, 2026]
**What I did**: Adding Feature 1 (Process Priority). 

**Details**: Modified the Process class to include a private int priority field. Updated the SchedulerSimulation class to generate a random integer between 1-5 during process creation. Added a print statement in addProcessToQueue to display the priority whenever a process enters the ready queue.

**Challenges**: Ensuring that each process gets a random priority between 1 and 5 and displays correctly.

**Solution**: Added a priority field in the Process class and used Random to assign values during creation.

**Time spent**: 1 hour.

---

### Entry 3 - [March 24, 2026]
**What I did**: mplementing Feature 2 (Context Switch Counter).

**Details**: Defined a public static int contextSwitchCount = 0 in the SchedulerSimulation class. Incremented this counter every time a thread was pulled from the queue and started. Added a final print statement at the end of the main method to report the total count.

**Challenges**: Determining the exact place in the scheduler loop to increment the static counter.

**Solution**: Placed the increment logic right before a new process starts its execution in the main loop.

**Time spent**: 45 mins.

---

### Entry 4 - [March 26, 2026]
**What I did**: Developing Feature 3 (Waiting Time Tracking).

**Details**: This was the most complex part. I added creationTime and totalWaitingTime to the Process class. I used System.currentTimeMillis() to capture the time when the process was created and updated the cumulative waiting time every time the process regained the CPU after being in the queue.

**Challenges**: Calculating the precise time spent in the ready queue without including execution time.

**Solution**: Used System.currentTimeMillis() to track when a process yields the CPU and when it starts again. 

**Time spent**: 2 hours.

---

### Entry 5 - [March 28, 2026]
**What I did**: Creating the summary table and finalizing documentation.

**Details**: Conducted a full simulation run to ensure the Round-Robin logic remained intact while new features worked. Formatted the final summary table using System.out.printf for better alignment. Completed the ANSWERS.md and REFLECTION.md files based on the simulation output. 

**Challenges**: Formatting the final output table to look professional and aligned in the console.

**Solution**: Used System.out.printf to format columns and verified all files against the final checklist.

**Time spent**: 1.5 hours.

---

### Entry 6 - [Optional - Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

## Summary

**Total time spent on assignment**: [Approximately 6-7 hours]

**Most challenging part**: The hardest part was calculating the Waiting Time correctly. I had to make sure I only count the time when the process is sitting in the queue, and not when it's actually running or before it was even created. Getting the math right with System.currentTimeMillis() took some trial and error.

**Most interesting learning**: It was really cool to see how Round-Robin works in a real Java program. I learned how Threads can be paused and started again, and how the 'Context Switch' happens. It made the theoretical parts of the OS class much easier to understand.
**What I would do differently next time**: Next time, I would start the documentation earlier while I'm coding so I don't forget the small details. I also want to learn more about how to handle multiple threads without using Thread.sleep(), maybe using more advanced synchronization.
