# 📝 MY_WORK: Student Information, Development Log, Reflection & Answers

> This is the **only file** your instructor reads to grade Parts 3 and 4 (documentation and video). Everything you write here must be **in your own words**.

---

## 🛑 STOP: Read This Before You Do Anything Else

> ### 1️⃣ Read the whole `README.md` first
> The `README.md` in this repository contains the full instructions: how this assignment continues Assignment 1, the Chapter 5 recap, class descriptions, feature specifications, question prompts and the video script. **If you skip it, you will lose marks.**
>
> ### 2️⃣ Understand the full code before answering any question
> Open `SchedulerSimulationSync.java` and read it **from top to bottom**. You must be able to explain what `SharedStats`, `ReadyQueue`, `CpuWorker`, `RaceWindow.pause()`, `ReentrantLock` and `Semaphore` do **before** you write a single answer in Parts B and C. **Run the original starter first** (it is intentionally broken) and **save its output**: you need it for Question 1 of Part C.
>
> ### 3️⃣ Use only the code of this repository
> Work **only** on `SchedulerSimulationSync.java` from this repository. Do **not** copy or paste code from your previous assignments.
>
> ### 4️⃣ Commit many times, not once
> A single commit, or all commits made in the last hour, costs you **-0.5 mark**. See the [Commit Rules](#-commit-rules-mandatory) below.

**How to use this file:**
1. Fill in your **Student Information** (below) right now.
2. Follow the steps in the **Work Roadmap** in order.
3. Update the **Development Log** *every time* you work on the assignment, not at the end.
4. Do not delete any section header. Replace the `[...]` placeholders with your own text.

---

## 👤 Student Information

> ⚠️ **WARNING:** Fill this in first. Your name and ID must match the student ID you set in `SchedulerSimulationSync.java` (line 304) and the one you say in your video.

| Field | Your Answer |
|-------|-------------|
| **Full Name** | leen ahmad ghazal |
| **Student ID** | 445052798 |
| **University Email** | 445052798@std.psau.edu.sa |
| **GitHub Username** | Leee82 |
| **Repository Link** | https://github.com/Leee82/OS-Assignment3-Starter-481-LEEN-GHAZAL |
 
---

## 🎥 Video Link

**Video Link**: [Paste your video link here]

> ⚠️ **WARNING:** The video must be **publicly accessible** ("Anyone with the link can view") on **Google Drive**, **YouTube (Unlisted or Public)** or any other cloud file-sharing system. A private, restricted or broken link counts as a **missing video (-1 mark)**.
>
> 💡 **TIP:** Open the link in a **private/incognito window** before you submit. If it asks you to log in or request access, it is not public.
>
> 📌 **NOTE:** The link goes in **this file only** (`MY_WORK.md`), **not** in `README.md`. Name your video file `StudentID_Assignment3_Demo.mp4`. It must last **2 to 3 minutes**.

---

## 🗺️ Work Roadmap (follow in this order)

| Step | What to do | Where | Marks |
|:----:|------------|-------|:-----:|
| 0 | Read `README.md`, read the full code, **run the original starter and save its output** (it fails on purpose) | Your IDE | – |
| 1 | Fork, rename, keep the repo **PUBLIC**, set your student ID (line 304), **commit** | GitHub + code | Part 1 (1) |
| 2 | Feature 1: Mutex lock on the ready queue, **commit** | Code | Part 2 (0.25) |
| 3 | Feature 2: Mutex lock(s) on the shared statistics, **commit** | Code | Part 2 (0.25) |
| 4 | Feature 3: Counting semaphore instead of busy waiting, **commit** | Code | Part 2 (0.5) |
| 5 | Development Log (5+ entries, different dates) | This file, Part A | Part 3 (0.5) |
| 6 | Reflection (4 questions) | This file, Part B | Part 3 (0.5) |
| 7 | Technical Answers (4 questions) | This file, Part C | Part 3 (0.5) |
| 8 | Record the video, upload it, paste the link above | Video + this file | Part 4 (1.5) |
| 9 | Final check, then submit the repo link on Blackboard | Blackboard | – |

> 💡 **TIP:** Tick each step off as you go. Do not leave the log, the reflection or the video for the last day.

---

## 🔁 Commit Rules (MANDATORY)

> ### ⚠️ MANY COMMITS ARE REQUIRED. A single bulk commit is penalized (-0.5 mark).

**Minimum: 4 meaningful commits. Aim for 7 or more.**

| # | Commit | Example message |
|:-:|--------|-----------------|
| 1 | Student ID set | `Set my student ID: 441234567` |
| 2 | Feature 1: Ready queue lock | `Feature 1: Protected the ready queue with a ReentrantLock` |
| 3 | Feature 2: Statistics locks | `Feature 2: Added locks to the shared statistics counters` |
| 4 | Feature 3: Semaphore | `Feature 3: Replaced busy waiting with a counting semaphore` |
| 5 | Development log entries | `Docs: Added development log entries 1-3` |
| 6 | Reflection and answers | `Docs: Completed reflection and technical answers` |
| 7 | Video link | `Docs: Added demo video link` |

**Rules:**
- ✅ **One commit per feature.** Do not put all three features in one commit.
- ✅ **Commit after each work session**, and after each part of this file.
- ✅ **Spread your commits over different dates.** Not all in one day.
- ❌ **Do not make all commits in the last hour** before the deadline (November 14, 2026).
- ❌ **No vague messages** like `done`, `update` or `final version`.

> 💡 **TIP:** Your commit history is checked and you **show it in your video** (at least 4 commits visible). Your development log dates should match your commit dates.
>
> 💡 **TIP:** **Use VS Code** (see *Recommended Development Environment* in `README.md` for the full setup). Sign in to GitHub in VS Code, then commit from the Source Control panel (Ctrl+Shift+G) → stage → write a message → Commit → Sync/Push. You can edit and commit this file the same way. **Pushing** matters: commits that are not pushed to GitHub are invisible to the instructor.

---

# Part A: Development Log (0.5 mark)

> ⚠️ **WARNING:** Minimum **5 entries**, spread over **different dates**. Five entries written on the same day, or written all at once at the end, will lose marks and look like a copy. Entry dates should be **between the start of the assignment and the deadline (November 14, 2026)**.
>
> 💡 **TIP:** Write an entry at the **end of each work session**, while you still remember what happened. It takes 5 minutes.
>
> 💡 **TIP:** Be specific. "Worked on the code" is a weak entry. "Added a `ReentrantLock queueLock` to `ReadyQueue` and wrapped the body of `poll()` in `lock()` / `try` / `finally { unlock() }`" is a strong one.
>
> 📌 **NOTE:** Each entry needs: date and time, what you did, details, challenges, solution, and time spent. Real challenges are fine (and expected). Do not invent fake ones.

## Example Entry (do not copy it, write your own)

### Entry 1 - [November 2, 2026, 4:30 PM]
**What I did**: Forked the repository, set my student ID, and ran the original starter

**Details**:
- Forked the starter repository and renamed it
- Changed student ID on line 304 to my actual ID (441234567)
- Ran the original program: 4 CPUs started, three of them picked `P1`, then `IllegalThreadStateException` and the watchdog stopped the program
- Saved the output in a text file for Question 1
- Committed and pushed: `Set my student ID: 441234567`

**Challenges**: I did not understand why the same process was picked by three CPUs

**Solution**: Read `ReadyQueue.poll()` again and found the `RaceWindow.pause()` between reading the head and removing it

**Time spent**: 45 minutes

---

## Your Development Log

### Entry 1 - [6/11/2026- 1:15pm]
**What I did**:
- first setups for the assignment
**Details**:
-forked the repository
-cloned on vs code
- changed id and studentinfo
**Challenges**:
- nothing really, everything was clear because i learned from assignment 1
**Solution**:
- none
**Time spent**:
-10 minutes
---

### Entry 2 - [7/11/2026, 9:17pm]
**What I did**:
- added feature 1
**Details**:
- added ReentrantLock lock
- imported concurrent.locks.ReentrantLock
- protected several methods and variables in readyqueue.
**Challenges**:
- what excatly that needed to be capsulated
**Solution**:
- figured what changes 
**Time spent**:
- 45 minutes
---

### Entry 3 - [7/11/2026 , 9:32pm]
**What I did**:
- added feature 2
**Details**:
- Added three locks (contextSwitchLock, completedProcessLock, serviceTimeLock), one per shared variable
- Wraped the three update methods and the three getters in lock() + try/finally unlock()
**Challenges**:
- none
**Solution**:
- it was prettu easy because i understood the idea in feature 1
**Time spent**:
- 15 minutes
---

### Entry 4 - [8/11/2026- 12:10pm]
**What I did**:
- modified feature 3
**Details**:
- Added a semaphore that counts the processes waiting in the ready queue, and add() releases it each time a process is added
- Each CPU blocks until a process is available instead of sleeping and polling
- When the last process completes, the CPU releases one permit per CPU so all the others wake up and stop cleanly
**Challenges**:
- Choosing the semaphore’s starting value
- CPUs hanging at the end
**Solution**:
- started it at 0, because the queue is empty at the start and each add() raises it by one.
- The CPU that sees all processes completed calls release(totalCPUs), so the blocked CPUs wake up and stop.
**Time spent**:
- 45 minutes
---

### Entry 5 - [Date and Time]
**What I did**:
completed the questions in mywork
**Details**:
- answered part b reflection
- answered part c technecial
**Challenges**:
- it was dense and long
**Solution**:
- completed it slowly
**Time spent**:
- 60 minutes
---

### Entry 6 - [Optional - Date and Time]
**What I did**:

**Details**:

**Challenges**:

**Solution**:

**Time spent**:

---

## Development Log Summary

> 💡 **TIP:** Fill this in **last**, after all entries are written.

**Total time spent on assignment**: [X hours]

**Most challenging part**:

**Most interesting learning**:

**What I would do differently next time**:

---

# Part B: Reflection (0.5 mark)

> 🛑 **STOP:** Do **not** start this part until you have read the `README.md`, read the **entire** `SchedulerSimulationSync.java`, run it, and finished the three features.
>
> ⚠️ **WARNING:** Each answer must be **5 to 7 sentences**, in **your own words**. Copied or AI-generated answers without understanding get **0 marks for the whole assignment**. You may be asked to explain them in person.
>
> 💡 **TIP:** Mention concrete things you actually did: a method you wrote, an error you hit, a line of output you saw. Generic answers score low.
>
> 💡 **TIP:** Draft your answer in a few bullet points first, then turn them into sentences.

## Question 1: What did you learn about synchronization?

> 💡 **TIP:** Talk about race conditions (read-modify-write), critical sections, mutual exclusion with `ReentrantLock` and `try/finally`, the role of a counting semaphore, and what surprised you when the starter failed.

**Your Answer:** *(5-7 sentences)*

i learned that something like count = count + 1 is not really one step, it reads the number, adds one, then writes it back. if two threads do it at the same time they can read the same number and one increment just disappears, thats the race condition. i used ReentrantLock with try/finally so only one thread can be in that part at a time and the lock always gets released. the semaphore was different, it just counts the processes in the queue so the cpu can sleep instead of checking again and again. what surprised me was that the starter looked fine but the numbers were wrong every time. also forgetting the shutdown signal made the whole program hang.

## Question 2: What was the most challenging part of this assignment?

> 💡 **TIP:** Pick **one** specific challenge (understanding why the starter failed, choosing the lock granularity, the initial value of the semaphore, the shutdown of the CPUs, Git, the video) and say *why* it was hard.

**Your Answer:** *(5-7 sentences)*

the most challenging part was implementing feature 3, especially the shutdown of the cpus. i understood that the last cpu had to wake up the others with release(totalCPUs), but where to put it was hard. it was tough because i had the old polling loop and my new while(true) loop mixed together, so the shutdown code ended up outside the loop and never ran. because of that the cpus crashed and the verification block was wrong for everything except the busy waiting polls. i only fixed it after checking the braces one by one and keeping a single while(true) loop with the shutdown check as the last thing inside it.

## Question 3: How did you overcome the challenges you faced?

> 💡 **TIP:** Describe your method: reading the slides and the documentation, adding `System.out.println` to debug, running the program many times, re-reading the README, testing after each small change, asking for help.

**Your Answer:** *(5-7 sentences)*

i overcame them by going step by step and testing after every small change instead of doing all three features at once. i re-read the slides and the readme a few times to make sure i understood what each feature wanted before touching the code. when the output was wrong i added System.out.println in different places to see which cpu was picking which process. i also ran the program many times because the race conditions did not show up every run. for the braces problem i went through them one by one until i knew exactly where the while(true), run() and the class ended.

## Question 4: Where can synchronization concepts be applied in real-world applications?

> 💡 **TIP:** Use real applications you know (banking and money transfers, ticket or seat booking, a shared counter on a website, a print queue, a database) and connect each one to what you built here (shared data, critical section, lock or semaphore).

**Your Answer:** *(5-7 sentences)*

synchronization is used in banking apps, for example when two people send money to the same account at the same time. the balance is shared data just like my counters, so without a lock one transfer could overwrite the other and money would disappear. ticket and seat booking works the same way, where the lock makes sure only one person can take the last seat. a print queue is like my ready queue, because a semaphore can count the waiting jobs and let the printer sleep until a new one arrives. websites with a shared counter, like likes or views, also need a lock so the number stays correct when thousands of users click at once.

### Optional: What would you like to learn more about?

[Any topics related to synchronization or operating systems that you're curious about?]

### Optional: How confident do you feel about synchronization concepts now?

[Beginner / Intermediate / Confident. What do you understand well? What needs more practice?]

### Optional: Feedback on the assignment

[Any comments? Was it helpful? Too easy or hard? Suggestions?]

---

# Part C: Technical Answers (0.5 mark)

> 🛑 **STOP:** You cannot answer these questions without understanding the code. Re-read `SchedulerSimulationSync.java` and **run it** first. Your answers must reference **your own code and your own output** (your student ID makes your output and your expected values unique).
>
> ⚠️ **WARNING:** Each answer must be **3 to 5 sentences**, with specific examples from your code or output. Use correct terms: race condition, critical section, mutual exclusion, mutex lock, semaphore, busy waiting, deadlock, producer, consumer.
>
> 💡 **TIP:** Keep the output of the **original starter** and the output of your **final version** in text files or screenshots, so you can copy real snippets for Question 1.

## Question 1: Race Condition in Your Own Output

**Question**: Run the **original starter** (before any fix) and paste the **verification block** of that run. Which value was wrong (expected vs observed)? Explain **step by step**, with two named threads/CPUs, how **one lost update** happens on one of the shared variables (read, `RaceWindow.pause()`, write). Why can the same bug happen on a real machine even without `RaceWindow`, and why is it hard to detect?

> ⚠️ **WARNING:** The snippet must come from **your own run** (with your student ID), not from a classmate or from this README.
>
> 💡 **TIP:** Use a small timeline: *CPU-1 reads `contextSwitchCount` = 12 → CPU-2 reads 12 → CPU-1 writes 13 → CPU-2 writes 13 → one increment is lost.* If your starter run crashed before printing numbers, run it several times (or paste the exception and the watchdog message and explain it).

**Your Answer:** *(3-5 sentences)*

all four values were wrong in my starter run: context switches 37 instead of 38, completed processes 15 instead of 16, service time 108338 instead of 111510, and busy waiting polls 742 instead of 0. the first three are lost updates, two cpus read the same old value, both add to it, and one increment disappears. the polls are not a race, it is just the cpus checking the empty queue again and again. the same bug can happen on a real machine without RaceWindow because count = count + 1 is really load, add, store, and a thread can be stopped or run on another core in the middle. it is hard to detect because it only happens when the timing is unlucky, so it does not crash and the program often looks fine.

Verification block of the **original starter**:
```
═══ VERIFICATION (expected values are computed from YOUR seed) ═══
  Context switches (quanta executed)     expected 38       observed 37       ? MISMATCH
  Completed processes                    expected 16       observed 15       ? MISMATCH
  Total service time (ms)                expected 111510   observed 108338   ? MISMATCH
  Busy-waiting polls (must be 0)         expected 0        observed 742      ? MISMATCH
  ? At least one check failed (see the ? lines above): a race condition or busy waiting is still present.


```

Verification block of **my final version**:
```
═══ VERIFICATION (expected values are computed from YOUR seed) ═══
  Context switches (quanta executed)     expected 38       observed 38       ?
  Completed processes                    expected 16       observed 16       ?
  Total service time (ms)                expected 111510   observed 111510   ?
  Busy-waiting polls (must be 0)         expected 0        observed 0        ?
  ? All shared values are consistent.
```

**Explanation of the timeline:**
1. CPU-1 reads contextSwitchCount and gets 12 (tmp = 12)
2. CPU-1 reaches RaceWindow.pause() and sleeps for 1 ms, still holding the old 12
3. CPU-2 reads contextSwitchCount, nobody has written yet so it also gets 12 (tmp = 12)
4. CPU-1 wakes up and writes 12 + 1 = 13
5. CPU-2 wakes up and writes 12 + 1 = 13


## Question 2: Critical Sections and Lock Granularity

**Question**: List the **critical sections** you protected (variables and methods) and the lock(s) you used. **Lock granularity:** did you use **one lock** for the three statistics or **one lock per variable**? Why, and what is the trade-off? Why is the **ready queue** protected by a **different** lock than the statistics? Explain how your solution provides **mutual exclusion**, and discuss **progress** and **bounded waiting** (a default `ReentrantLock` is not fair: what does that imply?).

> 💡 **TIP:** The three counters are independent: does updating `contextSwitchCount` need to block an update of `totalServiceTime`? Also think about what could go wrong (deadlock, or long waiting) if the queue lock and the statistics lock were the **same** lock and a thread held it while doing something slow.

**Your Answer:** *(3-5 sentences)*

| `ReadyQueue.add()` (`list`, `map`) | `lock` (ReadyQueue) | two cpus adding at the same time could corrupt the list and the map |
| `ReadyQueue.poll()` (`list`) | `lock` (ReadyQueue) | read head + remove head must be one step, or two cpus take the same process |
| `ReadyQueue.processOf()` (`map`) | `lock` (ReadyQueue) | a HashMap is not safe to read while another thread does put() |
| `ReadyQueue.snapshot()` (`list`, `map`) | `lock` (ReadyQueue) | looping over the list while it changes gives ConcurrentModificationException |
| `incrementContextSwitch()` / `getContextSwitchCount()` (`contextSwitchCount`) | `contextSwitchLock` | read-pause-write can lose an increment, and a getter could read in the middle of an update |
| `incrementCompletedProcess()` / `getCompletedProcessCount()` (`completedProcessCount`) | `completedProcessLock` | same lost update problem, and the shutdown check depends on this value being right |
| `addServiceTime()` / `getTotalServiceTime()` (`totalServiceTime`) | `serviceTimeLock` | same lost update problem on the total service time |

| Critical section (variable / method) | Lock used | Why it needs protection |
|---|---|---|
| [e.g., `ReadyQueue.poll()`] | [lock name] | [reason] |
| [...] | [...] | [...] |

## Question 3: Busy Waiting vs Semaphore

**Question**: Describe the **busy waiting** of the starter and its cost (give the `Busy-waiting polls` number from your **starter** run). What does the **value of your semaphore** represent? What is its **initial value** and why? What is its value right after the `numProcesses` initial `add()` calls? Why does the last CPU call `release(totalCPUs)` at the end, and what would happen if it did not?

> 💡 **TIP:** Think about what a CPU does when the queue is empty in the starter, and what a CPU does in your final version (is it running, ready or blocked?). Also check what happens to a CPU blocked in `acquire()` when no process will ever be added again.

**Your Answer:** *(3-5 sentences)*

in the starter a cpu that finds the queue empty sleeps 20 ms and checks again, over and over, so it wastes cpu time doing nothing, and my starter run showed 742 busy-waiting polls. my semaphore value is the number of processes waiting in the ready queue, it starts at 0 because the queue is empty when it is created, and after the 16 initial add() calls it is 16 (numProcesses), one release() for each process. in my final version an empty queue makes the cpu blocked in acquire() instead of running, so it uses no cpu time and the polls are 0. the last cpu calls release(totalCPUs) because no process will ever be added again, and the other cpus would stay blocked in acquire() forever, so the program would hang and only the watchdog would stop it

## Question 4: Classical Problems and Deadlock

**Question**: The CPUs and the ready queue look like a classical synchronization problem of Chapter 5. **Name it**, and say who plays the **producer** and the **consumer** roles (careful: here the CPUs also re-enqueue processes). If the ready queue were **bounded** (capacity `K`), name the **three semaphores** you would need and their **initial values**. Describe a **deadlock scenario** that appears if a thread acquired the **mutex before** waiting on the semaphore (or if two locks were acquired in different orders), and say **which of the four necessary conditions** you would break to prevent it.

> 💡 **TIP:** Recall the bounded-buffer solution of the slides (`empty`, `full`, `mutex`) and the order of `wait()` calls in the producer and the consumer. For the deadlock, think about a producer that holds the mutex while waiting for a free slot that only a consumer (who needs the mutex) can create.

**Your Answer:** *(3-5 sentences)*

**Classical problem and roles**:
producer-consumer problem (bounded buffer). the producers are the main thread (first adds) and a cpu that puts an unfinished process back with add(). the consumers are the cpus that take a process with acquire() and poll(). so every cpu plays both roles.

**Semaphores for a bounded queue (name and initial value)**:
- `empty` = K (the number of free slots, the queue starts empty)
- `full` = 0 (the number of processes in the queue, nothing at the start)
- `mutex` = 1 (only one thread can touch the queue at a time)

producer: wait(empty), wait(mutex), add, signal(mutex), signal(full).
consumer: wait(full), wait(mutex), remove, signal(mutex), signal(empty).

**Deadlock scenario and prevention**:
a cpu does wait(mutex) first and then wait(full) while the queue is empty. it is now blocked holding the mutex. a cpu that wants to add a process back needs that mutex to signal(full), so it waits forever, and both are stuck (the same happens in reverse if the queue is full and a producer holds the mutex while waiting for empty). the necessary condition i would break is hold and wait: always do wait(full) or wait(empty) first and take the mutex only after, so a thread never blocks while holding the mutex. for two locks taken in different orders, the broken condition would be circular wait, fixed by always taking them in the same order.

## Summary

**Key concepts I understood through these questions:**
1. a race condition happens because count = count + 1 is really read, add, write, so two threads can lose an update, and a lock with try/finally fixes it
2. one lock per independent variable is faster than one big lock, and the ready queue needs its own separate lock
3. a counting semaphore lets a cpu sleep until a process is available, and the last cpu must release(totalCPUs) or the others hang forever

**Concepts I need to study more:**
1. fair vs unfair locks and bounded waiting, because i only understand it in theory
2. the bounded-buffer problem with three semaphores and the order of the wait() calls, so i can spot deadlocks faster

---

# ✅ Final Checklist (complete before submitting)

> ⚠️ **WARNING:** Go through every line. Blackboard does not accept submissions after the deadline, which is **November 14, 2026**.

**Repository**
- [ ] Repository is **PUBLIC** (Settings → Danger Zone → Visibility)
- [ ] Repository is renamed to `OS-Assignment3-YourFirstName-YourLastName`
- [ ] GitHub account uses the university email (`@std.psau.edu.sa`)

**Code**
- [ ] Student ID is set in `SchedulerSimulationSync.java` (line 304)
- [ ] My code is based **only** on the starter of this repository (nothing copied from previous assignments)
- [ ] Code compiles and runs with no errors, and terminates by itself (no `⛔ WATCHDOG`)
- [ ] Feature 1 (ready queue lock), Feature 2 (statistics locks) and Feature 3 (semaphore, no busy waiting) all work
- [ ] **The four verification lines are ✔ in 5 consecutive runs**
- [ ] Every lock is released in a `finally` block
- [ ] `RaceWindow`, `Config`, the verification block and the watchdog are **unchanged**
- [ ] Each feature has clear comments

**Commits**
- [ ] **At least 4 meaningful commits, ideally 7 or more**
- [ ] **One commit per feature**
- [ ] Commits are spread over **different dates** (not all in the last hour)
- [ ] Everything is **pushed** to GitHub

**This file (`MY_WORK.md`)**
- [ ] Full name and student ID filled in at the top
- [ ] Development log has **5+ entries** on different dates
- [ ] Reflection: 4 questions, 5-7 sentences each
- [ ] Technical answers: 4 questions, 3-5 sentences each, with examples from **your** output (starter output **and** final output pasted in Question 1)
- [ ] No `[...]` placeholders left
- [ ] No section headers deleted

**Video**
- [ ] 2-3 minutes long, named `StudentID_Assignment3_Demo.mp4`
- [ ] Shows your name, ID, repository, 3 features (and your lock granularity choice), IDE execution with the verification block, one synchronization concept, and commit history
- [ ] Link is **public** (tested in an incognito window) and pasted in the **Video Link** section above

**Blackboard**
- [ ] Submit **only** the link to your public GitHub repository

> 🎯 **Good luck!** Start early, commit regularly, and make sure you can explain every line you submit.
