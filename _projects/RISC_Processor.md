---
layout: page
title: RISC-V Pipelined Processor
description: 5-stage RISC-V Processor with some advance features
img: assets/img/cpu.jpg
importance: 1
category: work
related_publications: 
---

By the collaboration of [Elijah Ye](https://elijah-ye.github.io), [Dongming Liu](https://github.com/MeanPaper), [Tracy Miao](https://github.com/tracymiao111) <br>
UIUC ECE411 FA23 | October 2023 ~ December 2023

For more details, please see the project github repository at this [link](https://github.com/Elijah-Ye/RISC-V_Pipelined_Processor).

## Running the Processor

### To run program without M-Extension

```
$ cd sram 
$ make
$ cd ..
$ make run_top_tb PROG=testcode/competition/coremark_rv32i.elf
$ make spike ELF=testcode/competition/coremark_rv32i.elf
$ diff -s sim/spike.log sim/golden_spike.log > sim/diff.log
$ cd synth
$ make synth
```
### To run program with M-Extension
```
$ cd sram 
$ make
$ cd ..
$ make run_top_tb PROG=testcode/competition/coremark_rv32im.elf
$ make spike ELF=testcode/competition/coremark_rv32im.elf
$ diff -s sim/spike.log sim/golden_spike.log > sim/diff.log
$ cd synth
$ make synth
```
### To run program with customized cache
You can change `localparam` in `mp4.sv` under `src/hdl/`. If you change the number of ways, you might need to regenerate plru update logic. You can do that by running `plru_update_generate.py` under `src/` with the correct number of ways.

<br>

## Documentation

| Check Point |
| - | :-: | :-: |
| **CP0** - Design Checkpoint |
| **CP1** - RV32I ISA, Basic Pipelining|
| **CP2** - Hazard Control, L1 Cache, <br> Forwarding, Static Branch Prediction |
| **CP3** - Advanced Design Options |
| **CP4** - Design Competition|

<br>

## Academic Integrity

Please review the University of Illinois Student Code,
particularly all subsections of [Article 1, Part 4 - Academic Integrity Policy and Procedure](https://studentcode.illinois.edu/article1/part4/1-401).



## Legal Notice

This work is protected under the [GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0.en.html). <br>
**Copyright (c) 2023 Elijah Gaohan Ye, Dongming Liu, Tracy Miao, Jian Huang**

    Permission to use, copy, modify, and distribute this software and its
    documentation for any purpose, without fee, and without written agreement
    is hereby granted, provided that the following two paragraphs appear
    in all copies of this software.

    IN NO EVENT SHALL THE AUTHOR OR THE UNIVERSITY OF ILLINOIS BE LIABLE TO
    ANY PARTY FOR DIRECT, INDIRECT, SPECIAL, INCIDENTAL, OR CONSEQUENTIAL
    DAMAGES ARISING OUT OF THE USE OF THIS SOFTWARE AND ITS DOCUMENTATION,
    EVEN IF THE AUTHOR AND/OR THE UNIVERSITY OF ILLINOIS HAS BEEN ADVISED
    OF THE POSSIBILITY OF SUCH DAMAGE.

    THE AUTHOR AND THE UNIVERSITY OF ILLINOIS SPECIFICALLY DISCLAIM ANY
    WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
    MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE. THE SOFTWARE
    PROVIDED HEREUNDER IS ON AN "AS IS" BASIS, AND NEITHER THE AUTHOR NOR
    THE UNIVERSITY OF ILLINOIS HAS ANY OBLIGATION TO PROVIDE MAINTENANCE,
    SUPPORT, UPDATES, ENHANCEMENTS, OR MODIFICATIONS.

> The software programs described in the documents are confidential and proprietary
> products of Synopsys Corp. or its licensors. The terms and conditions governing
> the sale and licensing of Synopsys products are set forth in written agreements
> between Synopsys Corp. and its customers. No representation or other affirmation
> of fact contained in this publication shall be deemed to be a warranty or give rise
> to any liability of Synopsys Corp. whatsoever. Images of software programs in use
> are assumed to be copyright and may not be reproduced.

> The documents are for informational and instructional purposes only. The ECE 411 teaching
> staff reserves the right to make changes in specifications and other information contained
> in this publication without prior notice, and the reader should, in all cases, consult
> the teaching staff to determine whether any changes have been made.