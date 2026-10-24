# AI-assisted exercise — Operating Systems

## Topic
Processes and threads

## Prompt used
> Explain the difference between a process and a thread in operating systems using a simple real-world example. Explain how memory is handled by processes and threads, and give two advantages of multithreading. Keep the explanation suitable for a B.Tech student.

## Tool and date
- **AI tool:** ChatGPT
- **Date:** 23 October 2026
- **Subject:** Operating Systems

## Summary of the response
The response described a process as a running program with its own virtual address space and a thread as a unit of execution inside a process. Threads in one process share code, global data and heap memory, but each thread has its own stack and CPU register state. The two advantages discussed were improved responsiveness and better resource utilisation; it also noted that shared memory requires care to avoid race conditions.

## Review and verification
I read the explanation and did not identify a correction to make. I did not verify it against a specific OS textbook or run a multithreading example. The description is a general model; details can vary by operating system and runtime.

## What I learned
I learned the main distinction between process isolation and thread-level sharing, including why threads can communicate efficiently but need synchronisation.

## Record status
The response was reviewed in this assignment session and no correction was reported. The review did not include a documented external-source check or independent practical test, so this file does not claim either one took place.
