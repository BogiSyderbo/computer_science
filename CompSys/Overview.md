CompSys is giving a general introduction to computer systems. You will learn how computers works at a basic but fundamental level, how this reflects to the programs that you write, and understand the performance characteristic for these. We will cover topics from Machine architecture, Operating Systems, Computer Networks, and basic IT-Security. We will also introduce you to the C programming language, which will be used throughout the course.

# Teaching material
- [COD] Computer Organization and Design, RISC-V Edition: The Hardware Software Interface, David A. Hennessy and John L. Patterson, 2nd edition, Morgan Kaufmann, ISBN: 978-0128203316
- [KR] Computer Networking: A Top-Down Approach, James F. Kurose and Keith W. Ross, Pearson, 8th and Global Edition, 2021, ISBN 13: 978-0135928608.
- [JG] Modern C, Jens Gustedt, Oct. 10, 2019, [http://modernc.gforge.inria.fr/](http://modernc.gforge.inria.fr/).
# Tools
- [RISC-V Interpreter](https://www.cs.cornell.edu/courses/cs3410/2019sp/riscv/interpreter/#)
- [Compiler Explorer](https://godbolt.org/)

# Assignments
- 6 assignments
- 4pts per assignment
- 50% (12pts) required for exam
- Assignments on Sundays
- In English or Danish

# Exam

Written final exam in English, this determines the final grade.

The exam is a written 4-hour open-book exam and will be held on Wednesday Jan 24.

The exam is *bring-your-own-device*.

Internet access, Google and LLMs(?) not allowed.

Questions split into: *Operating systems*, *Computer networks*, *micro-architecture*

## Resources/tools
- Books (COD, JG, OSTEP, KR, BOH, RISC-V)
- Slides and notes/links given for lectures
- DIKUNotes
- Recap slides
- RARS
- python3 (for number conversion, )
- Local LLM (ask about this ...)
- Scripts (DIKUNotes, your own, others ...)

### Games
- [Hexadecimal to binary conversion](http://topps.diku.dk/compsys/integers.html)
- [Cache](https://abdsecondhand.site/CACHE/dist/index.html)
- [Virtual table](https://abdsecondhand.site/VMAT/dist/index.html)
- [NANDGame](https://nandgame.com/)
- [RISC-V and C conversion](https://godbolt.org/)
- 

## Exam skills
- Conversion between hexadeciaml, binary, and decimal
- Assembly to C, C to assembly
- Loops in RISC-V
- Computer arithmetic
- Heap management
- Understand temporal and spatial locality
- Understand pipelining
- Drawing execution diagrams (afviklingsplot)
- Reading communication sequence diagrams (three-way-handshake)
- DNS, P2P, UDP, TCP
- Identify race conditions
- Data caching
- Understand semaphores
- Understand forks, threads, processes etc.
- Drawing *process graphs*!
- Network topology
- TCP transmission window size (see exercises 2024.01.03)
# Lecture plan for Computer Systems

| Week | Date | Topic | Lecture | Topic | Material |
| ---- | ---- | ---- | ---- | ---- | ---- |
| 36 | 04 Sep | Intro | Michael | Course introduction | COD 1.1-1.4,1.6-1.8 |
|  |  | Basic | David | Computers and C programming | JG 1-3 |
|  | 06 Sep | Basic | David | Assembly code and machine model | COD 2.1-2.4,2.6-2.7, JG 4 |
| 37 | 11 Sep | Basic | David | Functions and text | COD 2.8-2.9, JG 5-7 |
|  | 13 Sep | Basic | David | Computer arithmetic | COD 3.1-3.3, 3.5 |
| 38 | 18 Sep | Basic | David | C Programming - pointers and memory | JG 8-9, 11 |
|  | 20 Sep | Basic | David | C Programming - dynamic memory | JG 12-13 |
| 39 | 25 Sep | Basic | David | Memory hierarchy and caching | COD 5.1-5.4 |
|  | 27 Sep | OS | David | Intro to Operating systems - kernel, processes, system calls | OSTEP 2,4,5 |
| 40 | 02 Oct | OS | David | Virtual memory - hardware perspective | COD 5.7-5.8 |
|  | 04 Oct | OS | David | Virtual memory - OS perspective | [OSTEP](https://pages.cs.wisc.edu/~remzi/OSTEP/) 13,17 |
| 41 | 09 Oct | OS | David | Concurrency I | COD 6.1-6.2, 6.4-6.5 and [OSTEP](https://pages.cs.wisc.edu/~remzi/OSTEP/) 27 |
|  | 11 Oct | OS | David | Concurrency II | [OSTEP](https://pages.cs.wisc.edu/~remzi/OSTEP/) 29,30 |
| 43 | 23 Oct | CN | David | Introduction to Computer Networks | KR 1.1 - 1.6 (Optional read - [Internet history](https://www.internetsociety.org/internet/history-internet/brief-history-internet/)) |
|  | 25 Oct | CN | David | Network Programming | BOH 11.4 (Optional read - [Beej's Guide to Network Programming](http://beej.us/guide/bgnet/) and BOH 11.1-11.3, 11.6) |
| 44 | 30 Oct | CN | David | Non-Blocking Servers and Introduction to Security | BOH 12.1-12.3, KR 8.1, 8.2 |
|  | 01 Nov | CN | David | Network Applications: Application Design, Socket API, HTTP & Content Delivery | KR 2.1, 2.2, 2.3.1, 2.3.2, 2.6.1 - 2.6.3 |
| 45 | 06 Nov | CN | David | Application Layer: DNS + P2P File Distribution, Transport layer: UDP | KR 2.4, 2.5, 3.1 - 3.3 |
|  | 10 Nov | CN | David | Transport layer: Principles of Reliable Data Transfer + TCP | KR 3.1 - 3.7 |
| 47 | 20 Nov | CN | David | Server Performance | BOH 12.5-12.7 (Optional read - BOH 8.5-8.7) |
|  | 22 Nov | Arc | Finn | Et minimalt riscv setup | slides, TBD |
| 48 | 27 Nov | Arc | Finn | Digital logik | COD A.1 - A.3, A.5, A7 - A.9, [NandGame](https://nandgame.com/) |
|  | 29 Nov | Arc | Finn | En simpel maskine | COD 4.1 - 4.4 |
| 49 | 04 Dec | Arc | Finn | A5 - Simulation af en maskine. Riscv afkodning | RISCV 2.2 - 2.6 + 6 [RISCV](https://riscv.org/wp-content/uploads/2017/05/riscv-spec-v2.2.pdf) og lille note om afkodning |
|  | 06 Dec | Arc | Finn | Into til Mikroarkitektur: Pipelining og ydeevne | COD 4.6 - 4.9 |
| 50 | 11 Dec | Arc | Finn | Avanceret Mikroarkitektur I | COD 4.11 + [note](https://github.com/diku-compSys/compSys-e2023-pub/blob/main/resources/Afviklingsplot/plot.md) |
|  | 13 Dec | Arc | Finn. | Avanceret Mikroarkitektur II | [note](https://github.com/diku-compSys/compSys-e2023-pub/blob/main/resources/Afviklingsplot/plot.md) |
| 51 | 18 Dec | Arc | Finn. | Opsamling. Maskinnær optimering. A6 | TBD |
| 1 | 03 Jan | CN | Michael | Network layer, data plane | KR 4.1 - 4.2.4, 4.3 (Optional read - [Design Philosophy of DARPA Internet Protocols](http://www.cs.princeton.edu/courses/archive/spr14/cos461/papers/clark88.pdf)) |
| 2 | 08 Jan | CN | Michael | Network layer, control plane | KR 5.1 - 5.3, KR 6.1 - 6.4.3, KR 8.5 - 8.6 |
| 2 | 10 Jan | CN | Michael | Security Across the Network | KR 5.1 - 5.3, KR 6.1 - 6.4.3, KR 8.5 - 8.6 |
