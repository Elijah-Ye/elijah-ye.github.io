---
layout: page
title: VLSI Physical Design
description: Custom CMOS standard cells and datapath, from transistor layout to routed design
importance: 2
category: work
related_publications:
---

UIUC ECE425 SP26 | January 2026 ~ May 2026

This was a course project, so the design files are kept in a private repository per course policy.

## Overview

Working in the FreePDK45 process, I took a processor datapath from transistor-level cells all the way to a routed layout, using Cadence Virtuoso, Calibre, Synopsys Design Compiler, and Cadence Innovus.

## Standard Cell Library

- Built an area-optimized custom CMOS standard cell library (inverters, buffers, NAND/NOR, AND/OR, XOR/XNOR, AOI/OAI, multiplexers, latches, and flip-flops), verified via DRC, LVS, and digital simulation
- Optimized transistor sizing to balance strict area constraints with worst-case pull-up/pull-down drive strength equivalent to a minimum-size NMOS

## Datapath

- Designed the schematic and physical layout of a bit-sliced datapath with a custom ALU and register file

## Synthesis and Place-and-Route

- Ran Design Compiler synthesis and Innovus place-and-route, taking RTL to routed layout
