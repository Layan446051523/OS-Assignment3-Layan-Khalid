📝 MY_WORK: Student Information, Development Log, Reflection & Answers
Quote This is the only file your instructor reads to grade Parts 3 and 4 (documentation and video). Everything you write here must be in your own words.
🛑 STOP: Read This Before You Do Anything Else
Quote 1️⃣ Read the whole README.md first
The README.md in this repository contains the full instructions: how this assignment continues Assignment 1, the Chapter 5 recap, class descriptions, feature specifications, question prompts and the video script. If you skip it, you will lose marks.
2️⃣ Understand the full code before answering any question
Open SchedulerSimulationSync.java and read it from top to bottom. You must be able to explain what SharedStats, ReadyQueue, CpuWorker, RaceWindow.pause(), ReentrantLock and Semaphore do before you write a single answer in Parts B and C. Run the original starter first (it is intentionally broken) and save its output: you need it for Question 1 of Part C.
3️⃣ Use only the code of this repository
Work only on SchedulerSimulationSync.java from this repository. Do not copy or paste code from your previous assignments.
4️⃣ Commit many times, not once
A single commit, or all commits made in the last hour, costs you -0.5 mark. See the Commit Rules (#-commit-rules-mandatory) below.
How to use this file:
1. Fill in your Student Information (below) right now.
2. Follow the steps in the Work Roadmap in order.
3. Update the Development Log every time you work on the assignment, not at the end.
4. Do not delete any section header. Replace the [...] placeholders with your own text.
👤 Student Information
Quote ⚠️ WARNING: Fill this in first. Your name and ID must match the student ID you set in SchedulerSimulationSync.java (line 304) and the one you say in your video.
Table
🎥 Video Link
Video Link: https://drive.google.com/file/d/1VJ_UkDxyl82dhixR8gX25DXNx2-zuAOQ/view?usp=sharing
Quote ⚠️ WARNING: The video must be publicly accessible ("Anyone with the link can view") on Google Drive, YouTube (Unlisted or Public) or any other cloud file-sharing system. A private, restricted or broken link counts as a missing video (-1 mark).
💡 TIP: Open the link in a private/incognito window before you submit. If it asks you to log in or request access, it is not public.
📌 NOTE: The link goes in this file only (MY_WORK.md), not in README.md. Name your video file StudentID_Assignment3_Demo.mp4. It must last 2 to 3 minutes.
🗺 Work Roadmap (follow in this order)
Table
Quote 💡 TIP: Tick each step off as you go. Do not leave the log, the reflection or the video for the last day.
🔁 Commit Rules (MANDATORY)
Quote ⚠️ MANY COMMITS ARE REQUIRED. A single bulk commit is penalized (-0.5 mark).
Minimum: 4 meaningful commits. Aim for 7 or more.
Table
Rules:
- ✅ One commit per feature. Do not put all three features in one commit.
- ✅ Commit after each work session, and after each part of this file.
- ✅ Spread your commits over different dates. Not all in one day.
- ❌ Do not make all commits in the last hour before the deadline (November 14, 2026).
- ❌ No vague messages like done, update or final version.
Quote 💡 TIP: Your commit history is checked and you show it in your video (at least 4 commits visible). Your development log dates should match your commit dates.
💡 TIP: Use VS Code (see Recommended Development Environment in README.md for the full setup). Sign in to GitHub in VS Code, then commit from the Source Control panel (Ctrl+Shift+G) → stage → write a message → Commit → Sync/Push. You can edit and commit this file the same way. Pushing matters: commits that are not pushed to GitHub are invisible to the instructor.
Part A: Development Log (0.5 mark)
Quote ⚠️ WARNING: Minimum 5 entries, spread over different dates. Five entries written on the same day, or written all at once at the end, will lose marks and look like a copy. Entry dates should be between the start of the assignment and the deadline (November 14, 2026).
💡 TIP: Write an entry at the end of each work session, while you still remember what happened. It takes 5 minutes.
💡 TIP: Be specific. "Worked on the code" is a weak entry. "Added a ReentrantLock queueLock to ReadyQueue and wrapped the body of poll() in lock() / try / finally { unlock() }" is a strong one.
📌 NOTE: Each entry needs: date and time, what you did, details, challenges, solution, and time spent. Real challenges are fine (and expected). Do not invent fake ones.
Example Entry (do not copy it, write your own)
Entry 1 - [November 2, 2026, 4:30 PM]
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
Your Development Log
Quote 📌 NOTE: My instructor allowed me to submit after the deadline and to do the work in one session, so all my entries are on November 15, 2026, with the real times of each step.
Entry 1 - [November 15, 2026, 6:40 PM]
What I did: Set up my environment, forked the repository and set my student ID
Details:
- Forked makopt/OS-Assignment3-Starter-481, renamed it and kept it public
- Cloned it in VS Code and changed the student ID on line 304 to 446051523
- My parameters: 12 processes, time quantum 5000 ms, 3 CPUs
Challenges: The Run button did not appear in VS Code, so I could not run the Java file
Solution: Installed the Extension Pack for Java and reopened the repository folder, then the Run option appeared above main
Time spent: 60 minutes
Entry 2 - [November 15, 2026, 7:47 PM]
What I did: Feature 1, protected the shared ready queue with a ReentrantLock
Details:
- Added import java.util.concurrent.locks.ReentrantLock and declared queueLock in ReadyQueue
- Wrapped the bodies of add(), poll(), processOf() and snapshot() in queueLock.lock() / try / finally { queueLock.unlock() }
- Ran the program: no exception, every CPU picked a different process and Completed processes was 12 ✔, but Context switches was 21 instead of 24 and Total service time was 75595 and 70595 instead of 85595, and Busy-waiting polls was 30 and 31
- Committed and pushed: Feature 1: Protected the ready queue with a ReentrantLock
Challenges: My first git commit failed with "Author identity unknown", and the git config command gave "key does not contain a section" because the two dashes before global were changed into a long dash when I copied it
Solution: Ran git config user.name and git config user.email without the global option, then the commit and the push worked
Time spent: 15 minutes