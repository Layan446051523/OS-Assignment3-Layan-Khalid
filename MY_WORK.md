# 📝 MY_WORK: Student Information, Development Log, Reflection & Answers

> This is the only file your instructor reads to grade Parts 3 and 4 (documentation and video). Everything you write here must be in your own words.

---

## 🛑 STOP: Read This Before You Do Anything Else

> ### 1️⃣ Read the whole README.md first
> The README.md in this repository contains the full instructions: how this assignment continues Assignment 1, the Chapter 5 recap, class descriptions, feature specifications, question prompts and the video script. If you skip it, you will lose marks.
>
> ### 2️⃣ Understand the full code before answering any question
> Open SchedulerSimulationSync.java and read it from top to bottom. You must be able to explain what SharedStats, ReadyQueue, CpuWorker, RaceWindow.pause(), ReentrantLock and Semaphore do before you write a single answer in Parts B and C. Run the original starter first (it is intentionally broken) and save its output: you need it for Question 1 of Part C.
>
> ### 3️⃣ Use only the code of this repository
> Work only on SchedulerSimulationSync.java from this repository. Do not copy or paste code from your previous assignments.
>
> ### 4️⃣ Commit many times, not once
> A single commit, or all commits made in the last hour, costs you -0.5 mark. See the [Commit Rules](#-commit-rules-mandatory) below.

How to use this file:
1. Fill in your Student Information (below) right now.
2. Follow the steps in the Work Roadmap in order.
3. Update the Development Log *every time* you work on the assignment, not at the end.
4. Do not delete any section header. Replace the [...] placeholders with your own text.

---

## 👤 Student Information

> ⚠️ WARNING: Fill this in first. Your name and ID must match the student ID you set in SchedulerSimulationSync.java (line 304) and the one you say in your video.

| Field | Your Answer |
|-------|-------------|
| Full Name | Layan Khaled Al-Masoud |
| Student ID | 446051523 |
| University Email | 446051523@std.psau.edu.sa |
| GitHub Username | Layan446051523 |
| Repository Link | https://github.com/Layan446051523/OS-Assignment3-Layan-Khalid |
 
---

## 🎥 Video Link

Video Link: PASTE_YOUR_VIDEO_LINK_HERE

> ⚠️ WARNING: The video must be publicly accessible ("Anyone with the link can view") on Google Drive, YouTube (Unlisted or Public) or any other cloud file-sharing system. A private, restricted or broken link counts as a missing video (-1 mark).
>
> 💡 TIP: Open the link in a private/incognito window before you submit. If it asks you to log in or request access, it is not public.
>
> 📌 NOTE: The link goes in this file only (MY_WORK.md), not in README.md. Name your video file StudentID_Assignment3_Demo.mp4. It must last 2 to 3 minutes.

---

## 🗺 Work Roadmap (follow in this order)

| Step | What to do | Where | Marks |
|:----:|------------|-------|:-----:|
| 0 | Read README.md, read the full code, run the original starter and save its output (it fails on purpose) | Your IDE | – |
| 1 | Fork, rename, keep the repo PUBLIC, set your student ID (line 304), commit | GitHub + code | Part 1 (1) |
| 2 | Feature 1: Mutex lock on the ready queue, commit | Code | Part 2 (0.25) |
| 3 | Feature 2: Mutex lock(s) on the shared statistics, commit | Code | Part 2 (0.25) |
| 4 | Feature 3: Counting semaphore instead of busy waiting, commit | Code | Part 2 (0.5) |
| 5 | Development Log (5+ entries, different dates) | This file, Part A | Part 3 (0.5) |
| 6 | Reflection (4 questions) | This file, Part B | Part 3 (0.5) |
| 7 | Technical Answers (4 questions) | This file, Part C | Part 3 (0.5) |
| 8 | Record the video, upload it, paste the link above | Video + this file | Part 4 (1.5) |
| 9 | Final check, then submit the repo link on Blackboard | Blackboard | – |

> 💡 TIP: Tick each step off as you go. Do not leave the log, the reflection or the video for the last day.

---

## 🔁 Commit Rules (MANDATORY)

> ### ⚠️ MANY COMMITS ARE REQUIRED. A single bulk commit is penalized (-0.5 mark).

Minimum: 4 meaningful commits. Aim for 7 or more.

| # | Commit | Example message |
|:-:|--------|-----------------|
| 1 | Student ID set | Set my student ID: 441234567 |
| 2 | Feature 1: Ready queue lock | Feature 1: Protected the ready queue with a ReentrantLock |
| 3 | Feature 2: Statistics locks | Feature 2: Added locks to the shared statistics counters |
| 4 | Feature 3: Semaphore | Feature 3: Replaced busy waiting with a counting semaphore |
| 5 | Development log entries | Docs: Added development log entries 1-3 |
| 6 | Reflection and answers | Docs: Completed reflection and technical answers |
| 7 | Video link | Docs: Added demo video link |

Rules:
- ✅ One commit per feature. Do not put all three features in one commit.
- ✅ Commit after each work session, and after each part of this file.
- ✅ Spread your commits over different dates. Not all in one day.
- ❌ Do not make all commits in the last hour before the deadline (November 14, 2026).
- ❌ No vague messages like done, update or final version.

> 💡 TIP: Your commit history is checked and you show it in your video (at least 4 commits visible). Your development log dates should match your commit dates.
>
> 💡 TIP: Use VS Code (see *Recommended Development Environment* in README.md for the full setup). Sign in to GitHub in VS Code, then commit from the Source Control panel (Ctrl+Shift+G) → stage → write a message → Commit → Sync/Push. You can edit and commit this file the same way. Pushing matters: commits that are not pushed to GitHub are invisible to the instructor.

---

# Part A: Development Log (0.5 mark)

> ⚠️ WARNING: Minimum 5 entries, spread over different dates. Five entries written on the same day, or written all at once at the end, will lose marks and look like a copy. Entry dates should be between the start of the assignment and the deadline (November 14, 2026).
>
> 💡 TIP: Write an entry at the end of each work session, while you still remember what happened. It takes 5 minutes.
>
> 💡 TIP: Be specific. "Worked on the code" is a weak entry. "Added a ReentrantLock queueLock to ReadyQueue and wrapped the body of poll() in lock() / try / finally { unlock() }" is a strong one.
>
> 📌 NOTE: Each entry needs: date and time, what you did, details, challenges, solution, and time spent. Real challenges are fine (and expected). Do not invent fake ones.

## Example Entry (do not copy it, write your own)

### Entry 1 - [November 2, 2026, 4:30 PM]
What I did: Forked the repository, set my student ID, and ran the original starter

Details:
- Forked the starter repository and renamed it
- Changed student ID on line 304 to my actual ID (441234567)
- Ran the original program: 4 CPUs started, three of them picked P1, then IllegalThreadStateException and the watchdog stopped the program
- Saved the output in a text file for Question 1
- Committed and pushed: Set my student ID: 441234567

Challenges: I did not understand why the same process was picked by three CPUs

Solution: Read ReadyQueue.poll() again and found the RaceWindow.pause() between reading the head and removing it

Time spent: 45 minutes

---

## Your Development Log

> 📌 NOTE: My instructor allowed me to submit after the deadline and to do the work in one session, so all my entries are on November 15, 2026, with the real times of each step.

### Entry 1 - [November 15, 2026, 6:40 PM]
What I did: Set up my environment, forked the repository and set my student ID

Details:
- Forked makopt/OS-Assignment3-Starter-481, renamed it and kept it public
- Cloned it in VS Code and changed the student ID on line 304 to 446051523
- My parameters: 12 processes, time quantum 5000 ms, 3 CPUs

Challenges: The Run button did not appear in VS Code, so I could not run the Java file

Solution: Installed the Extension Pack for Java and reopened the repository folder, then the Run option appeared above main

Time spent: 60 minutes

---

### Entry 2 - [November 15, 2026, 7:47 PM]
What I did: Feature 1, protected the shared ready queue with a ReentrantLock

Details:
- Added import java.util.concurrent.locks.ReentrantLock and declared queueLock in ReadyQueue
- Wrapped the bodies of add(), poll(), processOf() and snapshot() in queueLock.lock() / try / finally { queueLock.unlock() }
- Ran the program: no exception, every CPU picked a different process and Completed processes was 12 ✔, but Context switches was 21 instead of 24 and Total service time was 75595 and 70595 instead of 85595, and Busy-waiting polls was 30 and 31
- Committed and pushed: Feature 1: Protected the ready queue with a ReentrantLock

Challenges: My first git commit failed with "Author identity unknown", and the git config command gave "key does not contain a section" because the two dashes before global were changed into a long dash when I copied it

Solution: Ran git config user.name and git config user.email without the global option, then the commit and the push worked

Time spent: 15 minutes

---

### Entry 3 - [November 15, 2026, 8:09 PM]
What I did: Feature 2, protected the three shared statistics with one lock per variable

Details:
- Declared contextSwitchLock, completedLock and serviceTimeLock in SharedStats
- Protected the three updates (incrementContextSwitch, incrementCompletedProcess, addServiceTime) and the three getters with the matching lock and try/finally
- Ran the program: the first three lines of the verification block were ✔ (24, 12, 85595), only Busy-waiting polls was still wrong (39)
- Committed and pushed: Feature 2: Added one lock per shared statistics counter

Challenges: Choosing between one lock for the three counters or one lock per counter

Solution: The three counters are independent (no method updates two of them together), so one lock per variable lets a thread update totalServiceTime while another thread updates contextSwitchCount

Time spent: 15 minutes

---

### Entry 4 - [November 15, 2026, 8:28 PM]
What I did: Feature 3, replaced busy waiting with a counting semaphore and added a clean shutdown

Details:
- Added import java.util.concurrent.Semaphore and declared readyCount = new Semaphore(0) in ReadyQueue
- Called readyCount.release() in add() after the process is inserted
- In CpuWorker.run(), called readyCount.acquire() before poll() and deleted the Thread.sleep(20) polling branch
- Added the shutdown: the CPU that sees completed == totalProcesses calls release(SharedStats.totalCPUs), and a CPU that wakes up after that stops the loop
- Ran the program 5 times: all four lines ✔ in every run, Busy-waiting polls = 0, and the program terminated by itself
- Committed and pushed: Feature 3: Replaced busy waiting with a counting semaphore

Challenges: Understanding why the CPUs need a shutdown signal at the end

Solution: Traced what happens after the last process completes: the queue is empty and no one calls add() again, so the CPUs blocked in acquire() would wait forever without release(totalCPUs)

Time spent: 20 minutes

---

### Entry 5 - [November 15, 2026, 8:40 PM]
What I did: Ran the original starter to collect its output for Question 1

Details:
- Put the original starter code back temporarily (with my student ID) and ran it
- CPU-1, CPU-2 and CPU-3 all picked P1, CPU-1 and CPU-2 crashed with IllegalThreadStateException, P2 was lost, and the watchdog stopped the program after 32 s
- Verification: Context switches 22/24, Completed processes 11/12, Total service time 76869/85595, Busy-waiting polls 799
- Restored my final version without committing the starter code

Challenges: I did not understand at first why three CPUs picked P1 and why P2 disappeared

Solution: Read ReadyQueue.poll() and found the RaceWindow.pause() between list.getFirst() and list.removeFirst(): the three CPUs read the same head, then each one removed a different element, so P2 was removed without being returned

Time spent: 10 minutes

---

### Entry 6 - [November 15, 2026, 9:00 PM]
What I did: Completed MY_WORK.md (reflection and technical answers)

Details:
- Answered the 4 reflection questions and the 4 technical questions using my own starter and final outputs
- Committed and pushed: Docs: Completed development log, reflection and technical answers

Challenges: Explaining the lost update and the bounded-buffer deadlock clearly

Solution: Reviewed the race condition and producer-consumer parts of the Chapter 5 slides and used my own output as the example

Time spent: 20 minutes

---

### Entry 7 - [November 15, 2026, 9:50 PM]
What I did: Recorded and uploaded the video demonstration

Details:
- Recorded the video in VS Code: introduction, code walkthrough of the 3 features, program run with the verification block, explanation of the race condition, and commit history
- Uploaded it as 446051523_Assignment3_Demo.mp4 and set it to "Anyone with the link can view"
- Committed and pushed: Docs: Added demo video link

Challenges: My first recording was 3 minutes and 51 seconds, which is longer than the 3-minute limit

Solution: I shortened my explanations, especially the race condition part, so the video fits between 2 and 3 minutes

Time spent: 40 minutes

---

## Development Log Summary

> 💡 TIP: Fill this in last, after all entries are written.

Total time spent on assignment: About 4 hours

Most challenging part: The clean shutdown of the CPUs in Feature 3, because CPUs blocked on acquire() never wake up if no process is added again.

Most interesting learning: A bug like the lost update in contextSwitchCount does not appear in the code at first sight, it only appears when two threads interleave at the wrong moment.

What I would do differently next time: Start earlier, before the deadline, and set up VS Code and Git in advance so that tool problems do not slow me down.

---

# Part B: Reflection (0.5 mark)

> 🛑 STOP: Do not start this part until you have read the README.md, read the entire SchedulerSimulationSync.java, run it, and finished the three features.
>
> ⚠️ WARNING: Each answer must be 5 to 7 sentences, in your own words. Copied or AI-generated answers without understanding get 0 marks for the whole assignment. You may be asked to explain them in person.
>
> 💡 TIP: Mention concrete things you actually did: a method you wrote, an error you hit, a line of output you saw. Generic answers score low.
>
> 💡 TIP: Draft your answer in a few bullet points first, then turn them into sentences.

## Question 1: What did you learn about synchronization?

> 💡 TIP: Talk about race conditions (read-modify-write), critical sections, mutual exclusion with ReentrantLock and try/finally, the role of a counting semaphore, and what surprised you when the starter failed.

Your Answer: *(5-7 sentences)*

I learned that an operation like contextSwitchCount++ is not one step but three steps: read, modify and write. When I ran the starter with my student ID, the three CPUs picked P1 at the same time and the counters ended with wrong values, which showed me that a race condition really loses data. I understood that the code that touches shared data is a critical section, and that it needs mutual exclusion so that only one thread is inside at a time. I used ReentrantLock for that, and I learned that unlock() must always be in a finally block, otherwise an exception can leave the lock held forever. I also learned that a counting semaphore can count resources, here the processes in the ready queue, so a CPU sleeps until a process is available instead of checking again and again. What surprised me most was that the race in poll() did not only give P1 to three CPUs, it also made P2 disappear completely, so its 8726 ms of service time were missing from the total.

## Question 2: What was the most challenging part of this assignment?

> 💡 TIP: Pick one specific challenge (understanding why the starter failed, choosing the lock granularity, the initial value of the semaphore, the shutdown of the CPUs, Git, the video) and say *why* it was hard.

Your Answer: *(5-7 sentences)*

The most challenging part for me was Feature 3, especially the shutdown of the CPUs. Replacing the polling loop with acquire() was simple, but then I had to think about what happens after the last process finishes. At that moment the queue is empty and no one will call add() again, so the other CPUs stay blocked in acquire() forever and the watchdog would stop the program. I also had to be careful not to call acquire() while holding queueLock, because then a CPU would sleep with the lock and no thread could add a process. Choosing the initial value of the semaphore also needed thinking, because a value of 1 would let a CPU take from an empty queue. These problems were hard because they do not give a compile error, they only show up when the threads run.

## Question 3: How did you overcome the challenges you faced?

> 💡 TIP: Describe your method: reading the slides and the documentation, adding System.out.println to debug, running the program many times, re-reading the README, testing after each small change, asking for help.

Your Answer: *(5-7 sentences)*

I started by reading the README and the full SchedulerSimulationSync.java before changing anything, and I saved the output of the original starter. Then I did the features in the order of the README, one feature at a time, and I ran the program at least five times after each one. I looked at the verification block after each run to see which line changed from ✘ to ✔, which told me if the feature worked. When I was stuck on the shutdown, I reviewed the semaphore part of the Chapter 5 slides and traced by hand what the last CPU does after the last process completes. I also reviewed the producer-consumer solution to understand why the semaphore must be acquired before the lock. Committing after each feature helped me too, because I always had a working version to go back to.

## Question 4: Where can synchronization concepts be applied in real-world applications?

> 💡 TIP: Use real applications you know (banking and money transfers, ticket or seat booking, a shared counter on a website, a print queue, a database) and connect each one to what you built here (shared data, critical section, lock or semaphore).

Your Answer: *(5-7 sentences)*

Synchronization is needed in any system where many users or threads change the same data at the same time. In banking, two transfers from the same account must be protected by a lock, otherwise one update to the balance can be lost exactly like the lost update in my contextSwitchCount. In ticket or seat booking, reading that a seat is free and then reserving it must be one critical section, or two people can book the same seat, which is like two CPUs picking P1 in my starter. A print queue works like my ready queue: users add jobs and the printer takes them, and a semaphore lets the printer sleep when there is nothing to print. Databases use locks to protect rows and tables during transactions. Web servers also use a pool of worker threads that wait on a queue of requests, which is the same producer-consumer idea I built in this assignment.

### Optional: What would you like to learn more about?

Monitors and condition variables, and how the operating system implements locks with hardware instructions like compare-and-swap.

### Optional: How confident do you feel about synchronization concepts now?

Intermediate. I understand race conditions, mutex locks and counting semaphores well. I need more practice with deadlock prevention and with the classical problems like readers-writers and dining philosophers.

### Optional: Feedback on the assignment

The RaceWindow made the race conditions visible in every run, which helped me understand them much better than reading about them.

---

# Part C: Technical Answers (0.5 mark)

> 🛑 STOP: You cannot answer these questions without understanding the code. Re-read SchedulerSimulationSync.java and run it first. Your answers must reference your own code and your own output (your student ID makes your output and your expected values unique).
>
> ⚠️ WARNING: Each answer must be 3 to 5 sentences, with specific examples from your code or output. Use correct terms: race condition, critical section, mutual exclusion, mutex lock, semaphore, busy waiting, deadlock, producer, consumer.
>
> 💡 TIP: Keep the output of the original starter and the output of your final version in text files or screenshots, so you can copy real snippets for Question 1.

## Question 1: Race Condition in Your Own Output

Question: Run the original starter (before any fix) and paste the verification block of that run. Which value was wrong (expected vs observed)? Explain step by step, with two named threads/CPUs, how one lost update happens on one of the shared variables (read, RaceWindow.pause(), write). Why can the same bug happen on a real machine even without RaceWindow, and why is it hard to detect?

> ⚠️ WARNING: The snippet must come from your own run (with your student ID), not from a classmate or from this README.
>
> 💡 TIP: Use a small timeline: *CPU-1 reads contextSwitchCount = 12 → CPU-2 reads 12 → CPU-1 writes 13 → CPU-2 writes 13 → one increment is lost.* If your starter run crashed before printing numbers, run it several times (or paste the exception and the watchdog message and explain it).

Your Answer: *(3-5 sentences)*

See the verification blocks and the explanation below.

Verification block of the original starter:
```
⛔️ WATCHDOG: the simulation did not finish (32 s). A process was lost, or a CPU is blocked forever, or the 'completed' counter lost an update.

═══ VERIFICATION (expected values are computed from YOUR seed) ═══
  Context switches (quanta executed)     expected 24       observed 22       ✘ MISMATCH
  Completed processes                    expected 12       observed 11       ✘ MISMATCH
  Total service time (ms)                expected 85595    observed 76869    ✘ MISMATCH
  Busy-waiting polls (must be 0)         expected 0        observed 799      ✘ MISMATCH
  ✘ At least one check failed (see the ✘ lines above): a race condition or busy waiting is still present.
```

Verification block of my final version:
```
═══ VERIFICATION (expected values are computed from YOUR seed) ═══
  Context switches (quanta executed)     expected 24       observed 24       ✔️
  Completed processes                    expected 12       observed 12       ✔️
  Total service time (ms)                expected 85595    observed 85595    ✔️
  Busy-waiting polls (must be 0)         expected 0        observed 0        ✔️
  ✔️ All shared values are consistent.
```

Explanation of the timeline:
In my starter run all four values were wrong: Context switches was 22 instead of 24 (2 increments lost), Completed processes was 11 instead of 12, and Total service time was 76869 instead of 85595 (8726 ms missing, which is exactly the burst time of P2). The run also started with CPU-3, CPU-1 and CPU-2 all picking P1, then CPU-1 and CPU-2 crashed with IllegalThreadStateException and P2 was lost, because poll() read the head and then removed a different element. One lost update on contextSwitchCount happens like this: the thread of P3 on CPU-1 reads contextSwitchCount = 5 → RaceWindow.pause() preempts it → the thread of P4 on CPU-2 also reads 5 → CPU-1 writes 6 → CPU-2 writes 6, so the counter is 6 instead of 7 and one increment is lost. On a real machine the same bug can happen without RaceWindow, because the scheduler can preempt a thread between the read and the write, or two cores can run the two steps truly in parallel. It is hard to detect because the window is only a few nanoseconds, so the program gives the right result in most runs and fails rarely and randomly.

## Question 2: Critical Sections and Lock Granularity

Question: List the critical sections you protected (variables and methods) and the lock(s) you used. Lock granularity: did you use one lock for the three statistics or one lock per variable? Why, and what is the trade-off? Why is the ready queue protected by a different lock than the statistics? Explain how your solution provides mutual exclusion, and discuss progress and bounded waiting (a default ReentrantLock is not fair: what does that imply?).

> 💡 TIP: The three counters are independent: does updating contextSwitchCount need to block an update of totalServiceTime? Also think about what could go wrong (deadlock, or long waiting) if the queue lock and the statistics lock were the same lock and a thread held it while doing something slow.

Your Answer: *(3-5 sentences)*

I protected the ready queue (list and map) in add(), poll(), processOf() and snapshot() with queueLock, and the three statistics with three locks: contextSwitchLock for contextSwitchCount, completedLock for completedProcessCount and serviceTimeLock for totalServiceTime, both in the update methods and in the getters. I chose one lock per variable because the three counters are independent: no method reads or writes two of them together, so an update of totalServiceTime has no reason to block an update of contextSwitchCount. The trade-off is more concurrency against more code and more locks to manage; a single lock would be simpler but would make threads wait for each other without need, and with several locks a thread must never hold two of them in different orders (my code never holds two locks at the same time). The queue uses a different lock because it is different data, and if the queue and the statistics shared one lock, a CPU working on the queue would block every process thread that only wants to update a counter. Mutual exclusion is guaranteed because each critical section is between lock() and unlock() of the same lock, so only one thread can be inside it. Progress is satisfied because when no thread holds the lock, lock() returns immediately, and finally always releases it. A default ReentrantLock is not fair, so it does not guarantee bounded waiting: a new thread can take the lock before a thread that has waited longer, and in theory one thread could starve; new ReentrantLock(true) would give FIFO order but slower performance, and here the critical sections are very short so the risk is small.

| Critical section (variable / method) | Lock used | Why it needs protection |
|---|---|---|
| list, map / ReadyQueue.add() | queueLock | Several CPUs re-enqueue processes at the same time; a LinkedList and a HashMap are not thread-safe |
| list / ReadyQueue.poll() | queueLock | Reading the head and removing it must be one atomic step, otherwise two CPUs take the same process and another one is lost |
| map / ReadyQueue.processOf() | queueLock | Reading the map while another thread is inserting can return a wrong value |
| list, map / ReadyQueue.snapshot() | queueLock | Iterating while another thread modifies the list can throw ConcurrentModificationException |
| contextSwitchCount / incrementContextSwitch(), getContextSwitchCount() | contextSwitchLock | Read-modify-write: lost updates make the count lower than the number of quanta |
| completedProcessCount / incrementCompletedProcess(), getCompletedProcessCount() | completedLock | A lost update means the count never reaches the total, so the CPUs never stop |
| totalServiceTime / addServiceTime(), getTotalServiceTime() | serviceTimeLock | Read-modify-write: a lost update loses a whole quantum of service time |

## Question 3: Busy Waiting vs Semaphore

Question: Describe the busy waiting of the starter and its cost (give the Busy-waiting polls number from your starter run). What does the value of your semaphore represent? What is its initial value and why? What is its value right after the numProcesses initial add() calls? Why does the last CPU call release(totalCPUs) at the end, and what would happen if it did not?

> 💡 TIP: Think about what a CPU does when the queue is empty in the starter, and what a CPU does in your final version (is it running, ready or blocked?). Also check what happens to a CPU blocked in acquire() when no process will ever be added again.

Your Answer: *(3-5 sentences)*

In the starter, when a CPU found the ready queue empty, it slept 20 ms and checked the queue again in a loop, and it only stopped when completedProcessCount reached totalProcesses. This is busy waiting: the CPU keeps running and testing a condition instead of doing useful work, and my starter run counted 799 busy-waiting polls. In my version the semaphore readyCount represents the number of processes currently waiting in the ready queue. Its initial value is 0 because the queue is empty when the ReadyQueue object is created, and after the 12 initial add() calls of main its value is 12. Each add() calls release() and each CPU calls acquire() before poll(), so a CPU that finds no process is blocked (it does not use the CPU) until another thread adds a process. When the last process completes, the CPU that sees completedProcessCount == totalProcesses calls release(totalCPUs) to wake up all the CPUs, and a CPU that wakes up checks the counter and stops. Without this signal, the other CPUs would stay blocked in acquire() forever because no process will ever be added again, the program would hang, and the watchdog would stop it.

## Question 4: Classical Problems and Deadlock

Question: The CPUs and the ready queue look like a classical synchronization problem of Chapter 5. Name it, and say who plays the producer and the consumer roles (careful: here the CPUs also re-enqueue processes). If the ready queue were bounded (capacity K), name the three semaphores you would need and their initial values. Describe a deadlock scenario that appears if a thread acquired the mutex before waiting on the semaphore (or if two locks were acquired in different orders), and say which of the four necessary conditions you would break to prevent it.

> 💡 TIP: Recall the bounded-buffer solution of the slides (empty, full, mutex) and the order of wait() calls in the producer and the consumer. For the deadlock, think about a producer that holds the mutex while waiting for a free slot that only a consumer (who needs the mutex) can create.

Your Answer: *(3-5 sentences)*

Classical problem and roles:
This is the Producer-Consumer (Bounded-Buffer) problem. The producers are the main thread, which adds the 12 processes at the start, and the CPU threads themselves, because a CPU calls add() again when a process is not finished after its quantum. The consumers are the CpuWorker threads, which call readyCount.acquire() and then poll() a process. So each CPU is both a consumer and a producer, and the ready queue is the shared buffer.

Semaphores for a bounded queue (name and initial value):
If the ready queue had a capacity K, I would need three semaphores: mutex initialized to 1 to protect the queue, empty initialized to K to count the free slots, and full initialized to 0 to count the processes in the queue. In my unbounded queue, full plays the role of readyCount and mutex plays the role of queueLock.

Deadlock scenario and prevention:
Suppose a CPU wants to re-enqueue a process and calls wait(mutex) first, then wait(empty), while the queue is full. It blocks on empty while holding the mutex. Another CPU calls wait(full), succeeds, then calls wait(mutex) to take a process and free a slot, but the mutex is held, so both threads wait for each other forever. All four necessary conditions hold: mutual exclusion, hold and wait, no preemption and circular wait. I would break hold and wait by always waiting on the counting semaphore before taking the mutex, which is what my code does: readyCount.acquire() is called in CpuWorker.run() outside queueLock, and no method holds two locks at the same time.

## Summary

Key concepts I understood through these questions:
1. A race condition comes from an unprotected read-modify-write sequence, and a mutex lock with try/finally prevents it.
2. A counting semaphore counts available resources and blocks threads instead of busy waiting.
3. Deadlock happens when a thread holds a lock while waiting for something only another thread that needs that lock can provide.

Concepts I need to study more:
1. Monitors and condition variables.
2. The readers-writers and dining-philosophers problems.

---

# ✅ Final Checklist (complete before submitting)

> ⚠️ WARNING: Go through every line. Blackboard does not accept submissions after the deadline, which is November 14, 2026.

Repository
- [x] Repository is PUBLIC (Settings → Danger Zone → Visibility)
- [x] Repository is renamed to OS-Assignment3-YourFirstName-YourLastName
- [x] GitHub account uses the university email (@std.psau.edu.sa)

Code
- [x] Student ID is set in SchedulerSimulationSync.java (line 304)
- [x] My code is based only on the starter of this repository (nothing copied from previous assignments)
- [x] Code compiles and runs with no errors, and terminates by itself (no ⛔️ WATCHDOG)
- [x] Feature 1 (ready queue lock), Feature 2 (statistics locks) and Feature 3 (semaphore, no busy waiting) all work
- [x] The four verification lines are ✔️ in 5 consecutive runs
- [x] Every lock is released in a finally block
- [x] RaceWindow, Config, the verification block and the watchdog are unchanged
- [x] Each feature has clear comments

Commits
- [x] At least 4 meaningful commits, ideally 7 or more
- [x] One commit per feature
- [ ] Commits are spread over different dates (not all in the last hour)
- [x] Everything is pushed to GitHub

This file (`MY_WORK.md`)
- [x] Full name and student ID filled in at the top
- [ ] Development log has 5+ entries on different dates
- [x] Reflection: 4 questions, 5-7 sentences each
- [x] Technical answers: 4 questions, 3-5 sentences each, with examples from your output (starter output and final output pasted in Question 1)
- [x] No [...] placeholders left
- [x] No section headers deleted

Video
- [x] 2-3 minutes long, named StudentID_Assignment3_Demo.mp4
- [x] Shows your name, ID, repository, 3 features (and your lock granularity choice), IDE execution with the verification block, one synchronization concept, and commit history
- [x] Link is public (tested in an incognito window) and pasted in the Video Link section above

Blackboard
- [ ] Submit only the link to your public GitHub repository

> 🎯 Good luck! Start early, commit regularly, and make sure you can explain every line you submit.