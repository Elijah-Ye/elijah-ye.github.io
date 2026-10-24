---
layout: page
title: Linux Kernel
description: x86 operating system kernel with multiple terminals, scheduling, and paging
importance: 5
category: work
github: https://github.com/Elijah-Ye/Linux_Kernel
related_publications:
---

UIUC ECE391 FA22 | October 2022 ~ December 2022

For more details, please see the project github repository at this [link](https://github.com/Elijah-Ye/Linux_Kernel).

## Overview

As a team, we built a Linux-like operating system kernel for x86 from the ground up in C and x86 assembly. It boots, runs user programs from its own file system, and supports 3 terminals with up to 6 concurrent processes.

## Features

- **Interrupts and exceptions:** IDT setup, i8259 PIC, and handlers for the keyboard, RTC, and PIT
- **System calls:** 10 system calls dispatched from user programs, enough to run a shell and utilities such as `ls`, `cat`, and `grep`
- **Paging:** 4kB and 4MB pages, including per-process program memory and video memory mapping
- **File system:** read-only file system for loading files and executables
- **Scheduling:** PIT-driven round-robin scheduling across processes in 3 terminals
- **Terminals:** 3 terminals with keyboard switching, each running its own shell, with per-terminal RTC frequency virtualization
