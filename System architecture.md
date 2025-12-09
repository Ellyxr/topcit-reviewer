

## I. System Concept

System architecture is crucial for implementing and operating information systems, delivering services through a combination of information technology (IT), hardware, and software[cite: 462]. It is growing in complexity due to new technologies like big data, cloud computing, and IoT[cite: 463]. Fundamentally, system architecture defines the structure, components, and relationships within an information system[cite: 464].

### I.01 Concept of System Architecture

#### A) Understanding System Architecture

| Concept | Description |
| :--- | :--- |
| **System Architecture (Broad Sense)** | Refers to all architecture (Application Architecture (AA), Data Architecture (DA), and Technical Architecture (TA)) for constructing an information system[cite: 465]. It is a document defining the structure to support business processes[cite: 466]. |
| **System Architecture (Narrow Sense)** | Defines system components (hardware, software, security, interactions)[cite: 467]. Specifically refers to **Technical Architecture (TA)** and defines the layout and connection of middleware, DB server, WAS, storage, and network for distributing application programs[cite: 468]. |

---

**Components of System Architecture (Broader Sense)** [cite: 469]
1.  Application Architecture (AA)
2.  Data Architecture (DA)
3.  Technical Architecture (TA)

**Components of Detailed System Architecture (Narrower Sense)**
* **Server design architecture:** Defines server resources, CPU clock speed/number of cores, memory capacity, network card performance, storage units, server type (e.g., 1U to 4U blade type), and server size (e.g., 1TB to 4 units)[cite: 470].
* **Network design architecture:** Defines network components, external networks capacity (bandwidth), switched/router determination, L4 switches for load balancing, security systems (DDNS, IPS, firewalls), and network addressing services (Subnet, IP, gateway)[cite: 471].
* **Storage design architecture:** Defines separate network storage, storage capacity/performance (IOPS, bandwidth), media types (SSD, SAS, SATA), RAID configuration type, and storage network type (SAN, ISCSI, NFS)[cite: 472].

#### B) Components of Information System

System components are items that provide the functions of an information system[cite: 473]. Detailed components include computer hardware, OS, and middleware running on a physical server[cite: 474].

* **Server:** Provides the computing power to process business logic and data by running application programs[cite: 475].
    * **Server Types:** Mainframes, Unix servers, and x86 servers are commonly used[cite: 476].
    * **Example:** A server providing web services includes a webserver, a Web Application Server (WAS), and a database server[cite: 477].
* **Network:** Connects the information system components for communication[cite: 478]. Devices include switches, routers, load balancers, and bridges[cite: 478].
* **Storage:** Holds the data of an information system[cite: 479].
    * **Types:** Block storage, File storage, and Object storage[cite: 479].
    * **Connection Methods:** Network attached storage (NAS), Storage area network (SAN), and Direct attached storage (DAS)[cite: 480].
* **Security:** Configured via the network connection, involving hardware (DDoS defense, firewalls) and software (monitoring, logging, blocking network traffic, IPS/IDS)[cite: 481].

### I.02 Types of System Architecture

#### B) Classification According to System Layout

| Type | Detail | Disadvantage |
| :--- | :--- | :--- |
| **Centralized architecture** | All systems are integrated in a single centralized place[cite: 482]. Uses an integrated database on a large-capacity server, offering simple configuration and ensuring data integrity[cite: 483]. | Load is concentrated during peak time[cite: 484]. |
| **Multi-region distributed system architecture** | Operations and application systems are distributed regionally, managing distributed data using small or medium-sized servers[cite: 485]. Reduces the load of each server and distributes user load[cite: 486]. | Makes it difficult to manage data integrity and makes system configuration complex[cite: 487]. |

#### C) Classification According to How Application Programs Are Provided

1.  **Client-server architecture:** Places system functions in the servers and configures clients to use the service[cite: 488].
    * **Service Types:** Games, chatting, messenger, FTP servers, and terminal servers[cite: 489].
2.  **Web system architecture:** The client uses a web browser to access application programs running on the server[cite: 490].
    * **Detail:** Generally consists of a webserver, a web application server, and a database server[cite: 491]. Performance and program reusability are high[cite: 492].

#### D) Classification by System Layer

This classification divides the information system into logical layers: presentation, business logic, and data layers[cite: 493]. Physical implementation can follow N-tier structures (two-tier or three-tier)[cite: 493].

* **Two-tier architecture:** Stores and processes data in the server and processes business logic and presentation for the client[cite: 494].
    * **Limitation:** Performance degrades as the number of users increases; disadvantageous in terms of scalability and reusability[cite: 495].
* **Three-tier architecture:** Designed to overcome the limitations of the two-tier architecture, introducing an additional tier between presentation and data tiers[cite: 496].
    * **Advantages:** Business logic is flexible and scalable; simplifies database access management; distribution of presentation tier simplifies development[cite: 497].
    * **Example:** Client (Presentation), WAS (Business Logic), DB (Data Layer)[cite: 498].

### I.03 Server's Stack Architecture

The server has a stack structure: computer hardware is at the bottom, followed by OS, middleware/platform, and the application program at the top[cite: 499].

* **Middleware/Platform:** Abstracts computer hardware and provides services to software[cite: 500].
    * **Role:** Supports the flexibility of convenient expansion/reduction of application programs and hardware independence[cite: 501].
* **Application Programs:** Provide services to users using this middleware[cite: 502].

---

## II. Network Concept

This section introduces network protocols, the OSI Reference Model, and the TCP/IP Protocol Suite, detailing data encapsulation and transfer across network layers[cite: 503]. It emphasizes the structure of the OSI 7 layers and the functions of key protocols and organizations[cite: 504].

### II.01 What is the Protocol?

A protocol is a standardized communication rule for sending and receiving data through a network[cite: 505].

**Standardization Organizations (Examples)**
* **IETF (Internet Engineering Task Force):** Responsible for most Internet-related standards[cite: 506].
* **3GPP (3rd Generation Partnership Project):** Responsible for wireless communication protocols (GSM, CDMA, LTE)[cite: 507].
* **ITU-T:** Responsible for protocols related to telephones[cite: 507].

### II.02 OSI Reference Model and TCP/IP Protocol Layer Structure

#### A) OSI Reference Model (7 Layers)

The OSI model describes the network communication process in seven layers[cite: 508].

| Layer | Protocol Examples | Function |
| :--- | :--- | :--- |
| **Application** | HTTP, SMTP, SNMP, FTP, Telnet, etc. [cite: 509] | Provides services for application programs, such as a user interface, email, and database management[cite: 509]. |
| **Presentation** | JPEG, MPEG, XDR, etc. [cite: 510] | Supports the syntax of data exchanged between two systems; performs encoding/encryption[cite: 510]. |
| **Session** | TLS, SSH, RPC, NetBIOS, etc. [cite: 511] | Responsible for communication sessions; establishes, maintains, and synchronizes interaction between devices[cite: 511]. |
| **Transport** | TCP, UDP, SCTP [cite: 512] | Provides reliable message transfer between end-to-end processes, including error control[cite: 512]. |
| **Network** | IP, IPX, ICMP, X.25, ARP, OSPF, etc. [cite: 513] | Supports packet transmission between networks from sending point to destination[cite: 513]. |
| **Data Link** | Ethernet, token ring, wireless LAN, etc. [cite: 514] | Provides the function of transferring frames between hops without error[cite: 514]. |
| **Physical** | Radio wave, optical fiber, PSTN, etc. [cite: 515] | Transfers the actual bits through physical media[cite: 515]. |

#### B) TCP/IP Protocol Suite (Mapping to OSI)

The TCP/IP model consolidates the upper layers of the OSI model[cite: 516].

1.  **Application layer:** Corresponds to the OSI Application, Presentation, and Session layers[cite: 517].
    * **Example:** HTTP, DNS, Telnet, FTP, email protocols (SMTP/POP3/IMAP4)[cite: 518].
2.  **Transport layer:** Responsible for data exchange between abstract ports, handled by applications using TCP, UDP, and SCTP[cite: 519].
3.  **Internet layer (Network layer):** Responsible for addressing and routing functions[cite: 520].
    * **Protocols:** IP, ICMP, IGMP, ARP (IP to MAC address conversion), and RARP (MAC address to IP conversion)[cite: 521].
4.  **Network interface layer:** Corresponds to the OSI Data Link and Physical layers[cite: 522].
    * **Responsibility:** Sending/receiving TCP/IP packets through physical media (e.g., IEEE 802.3 Ethernet, 802.11 WiFi)[cite: 523].

### II.03 Internet Address System

* **MAC address (Medium Access Control):** A physical or Ethernet hardware address (EHA) used to transfer frames between physically connected nodes[cite: 524]. It is **48 bits long**[cite: 524].
* **IP address (Internet Protocol):** A logical address system used to transfer datagrams between two hosts/routers[cite: 525]. IPv4 addresses are **32 bits**[cite: 526].
* **Port number:** A **16-bit** number used to transfer messages between two running processes (applications)[cite: 527].
    * **Well-known ports (0 to 1023):** Allocated by IANA (e.g., HTTP port 80)[cite: 528].
    * **Registered ports (1024 to 49,151):** Allocated by IANA[cite: 528].
    * **Dynamic ports (49,152 to 65,535):** Mostly used as a temporary number by clients[cite: 529].

---

## III. Operating System (OS)

The Operating System (OS) manages limited computer resources and provides services to users[cite: 530]. This section covers OS functions (process, memory, file management), process/thread lifecycle, deadlock, memory management techniques, and virtual memory[cite: 531].

### III.01 Operating System (OS)

* **OS Definition:** System software that provides a computer resource interface to users or application programs by efficiently managing the limited resources of computer hardware[cite: 532].

#### B) Main Functions of OS

1.  **Process management:** Includes creating, disposing, and terminating processes, managing pre-processes, providing communication/synchronization techniques, and preventing deadlock[cite: 533].
2.  **Main memory unit management:** Tracking and managing memory space/users, deciding which process occupies space, and allocating/recovering memory space[cite: 534].
3.  **File management:** Handles creation/disposal of files and directories, provisioning primitive management, and mapping files to auxiliary memory unit[cite: 535].
4.  **Input/output system management:** Manages I/O devices (mouse, keyboard, printer)[cite: 536].
5.  **Auxiliary memory unit management:** Handles storage allocation and disk scheduling[cite: 537].
6.  **Networking:** Manages distributed systems via the network by handling scattered programs[cite: 538].

#### C) Types of Main OS

| Category | OS Examples | Key Characteristics |
| :--- | :--- | :--- |
| **PC OS** | Windows, Mac OS [cite: 539] | Windows: stable, standardized GUI; Mac OS: optimized for Apple's hardware[cite: 539]. |
| **Mobile OS** | Android, iOS [cite: 540] | Android: high openness, APK file installation; iOS: very secure, AppStore installation only[cite: 540]. |
| **Server OS** | UNIX, Linux, Windows Server [cite: 541] | UNIX: multi-user environment, proprietary; Linux: open-source, lowest cost (Redhat/CentOS/Ubuntu types)[cite: 541]. |

### III.02 Process and Thread

#### A) Understanding of Process

* **Process:** Refers to a running program[cite: 542]. It is a work unit that allocates and uses various resources[cite: 543].

**Process Status Change (Lifecycle)**
* **New:** Process is created but not running[cite: 544].
* **Preparing/Ready:** Process is waiting for CPU allocation[cite: 545].
* **Running:** Process has the CPU allocation[cite: 545].
* **Finished:** Process has completed its running, and CPU allocation is released[cite: 546].
* **Standby/Wait:** Process ran after getting CPU allocation but is waiting for an event (input/output completion)[cite: 547].

* **Process Control Block (PCB):** Stores necessary process management information, including PID, status, program counter, scheduling priority, registered information, and main memory unit information[cite: 548].

#### C) Thread

* **Thread:** A basic unit for using a CPU, called a lightweight process[cite: 549]. A process generally has one or more threads[cite: 549].
* **Detail:** Threads share the memory unit (code, data, files) but create their own register and stack[cite: 550]. They require less CPU time for context exchange than processes because they share memory[cite: 551].
* **Multi-thread:** When a single process has multiple threads, allowing the CPU to occupy one thread at a time[cite: 552].

### III.03 Process Synchronization and Deadlock

#### A) Concept of Process Synchronization

Process synchronization is needed for protection when two or more parallel processes access and change the same data simultaneously (race condition)[cite: 553].

#### B) Critical Section Problem

* **Critical Section:** A section of code where processes change data shared with other processes[cite: 554].
* **Required Conditions for Solving the Critical Section Problem:**
    1.  **Mutual exclusion:** Only one process can use the shared resource at a time[cite: 555].
    2.  **Progress:** Only processes not running in the remainder section can enter a critical section without delay[cite: 556].
    3.  **Bounded waiting:** Limits the time allowed for processes to enter the critical section[cite: 557].

#### D) Deadlock Status

* **Deadlock:** Occurs when multiple processes compete over limited resources, and a process requests an unavailable resource, resulting in perpetual blocking[cite: 558].
* **Conditions Causing Deadlock:**
    1.  **Mutual Exclusion:** Only one process can use the shared resource[cite: 559].
    2.  **Hold & wait:** Processes are requesting other resources while occupying current resources[cite: 560].
    3.  **Non-preemption:** Resource allocation cannot be forcibly released until completion[cite: 561].
    4.  **Circular wait:** Resource requests form a circular chain[cite: 561].

**Ways to Solve Deadlock State:**
* **Prevention:** Removes the deadlock causing conditions in advance[cite: 562].
* **Avoidance:** Does not remove the condition but avoids it[cite: 563].
* **Detection:** Allows the deadlock condition to occur and resolves it[cite: 564].
* **Recovery:** Restarts the deadlocked process or restores it to the original state[cite: 565].

### III.04 Memory Unit Management

#### B) Memory Unit Management Technique

1.  **Memory unit allocation technique:** Searches for the best way to allocate processes to the available main memory area[cite: 566].
    * **First-fit:** Allocates the memory unit using the first searched space. Increases fragmentation[cite: 567].
    * **Best-fit:** Allocates the memory unit using the smallest available space that can meet requirements[cite: 568].
    * **Worst-fit:** Allocates the memory unit using the largest available space[cite: 569].
2.  **Fragmentation problem:** Memory space is wasted after request/recollection[cite: 570].
    * **External fragmentation:** Memory is split into unusable small spaces[cite: 571].
    * **Internal fragmentation:** Memory is partitioned into a fixed size, and if a process needs less space, the remaining space is wasted[cite: 573].
3.  **Solving the fragmentation problem:**
    * **Compaction technique:** Merges small-sized available memory to remove external fragmentation[cite: 574].
    * **Coalescing technique:** Merges spaces with adjacent addresses in the unused empty space list to create a larger space[cite: 575].

### III.05 Scheduling

* **Purpose of scheduling:** Allocates processes to the CPU efficiently[cite: 576]. Goals include maximizing throughput, minimizing response time, preventing system overload, and ensuring fairness[cite: 577].

#### B) Type and Characteristics of Scheduling

* **Preemptive scheduling:** CPU resources can be taken while another process is occupying them[cite: 578].
* **Non-preemptive scheduling:** CPU resources cannot be allocated to another process until the current task is completed[cite: 579].

**Types of Scheduling Algorithms (Examples)**

| Type | Method | Class |
| :--- | :--- | :--- |
| **FIFO (First In First Out)** | Allocates CPU in the order they are requested[cite: 580]. | Non-preemptive [cite: 580] |
| **SJF (Shortest Job First)** | Allocates CPU to the process with the shortest expected job time[cite: 581]. | Non-preemptive [cite: 581] |
| **SRT (Shortest Remaining Time)** | Allocates CPU to the process with the shortest expected remaining job time (SJF considered preemptive)[cite: 582]. | Non-preemptive [cite: 582] |
| **R-R (Round Robin)** | Allocates CPU resources according to a time slice, considered a preemptive FIFO process[cite: 583]. | Preemptive [cite: 583] |
| **MLQ (Multi-Level Queue)** | Processes different jobs by time slice in each queue[cite: 584]. | Preemptive [cite: 584] |

### III.06 Virtual Memory Unit

* **Virtual Memory:** A technique that solves the OS's limited memory space problem by using large-capacity auxiliary memory as main memory[cite: 585]. The virtual memory unit is logically used[cite: 585].

#### A) Implementing a Virtual Memory Unit

* **Paging technique:** Partitions main memory into fixed-sized **frames**, and process storage into fixed-sized **pages**, which are loaded into the frame[cite: 586].
* **Segmentation technique:** Partitions process storage into logical units (**segments**), and then loads them into the memory unit[cite: 587].

#### B) Page Replacement Technique

Used when memory pages are full and free space must be created[cite: 588].

* **Optimal technique:** Replaces a page not likely to be used for the longest time (theoretical optimal replacement)[cite: 589].
* **FIFO (First In First Out) technique:** Replaces the first loaded page[cite: 590].
* **LRU (Least Recently Used) technique:** Replaces the page that has been unused for the longest time[cite: 591].

#### C) Factors Affecting Virtual Memory Unit Performance

* **Locality:** Tendency for programs to reference a specific area intensively[cite: 592]. Divided into temporal and spatial locality[cite: 592].
* **Working Set:** A set of frequently referenced pages[cite: 593].
* **Thrashing:** A phenomenon where CPU utilization rate decreases because page replacement takes longer than processing[cite: 594].

### III.07 File System

* **File system:** Stores related data to find and access OS data and programs quickly[cite: 595].
* **File attributes:** Include name, type, location, size, protection, time, and date/user identification[cite: 596].

#### C) Allocation by a File System

The OS's file system generally uses three methods for disk space allocation[cite: 597].

1.  **Contiguous allocation:** Arranges files as a set of contiguous addresses on the physical disk[cite: 598]. Fast read speed, but creates external fragmentation[cite: 598].
2.  **Linked allocation:** Stores files in blocks and links each block to a list using pointers[cite: 599]. Solves external fragmentation but access is slow[cite: 599].
3.  **Indexed allocation:** Manages all pointer data in an index block[cite: 600]. Solves the problem of scattered block pointer addresses and does not create external fragmentation[cite: 600].

#### E) UNIX i-node

* **i-node (index node):** Component of the UNIX file system that handles allocation, application, creation, link, and deletion of file/directory data[cite: 601].
    * **i-node component:** Contains all the data of a file or directory, owner information, access information, file information, and type[cite: 602].
    * **i number:** An entry number of an i-node registered in the i-list[cite: 602].

---

## IV. Computer Architecture

Computer architecture is the conceptual design and operational structure that serves as the basis for computer systems[cite: 604]. This section details basic computer structure, compares Von Neumann and Harvard architectures, describes the CPU, memory hierarchy, and I/O devices (including DMA)[cite: 605, 606].

### IV.01 Computer Structure and Architecture

#### A) Basic Computer Structure

The basic function of a computer is to run a program code in a specified sequence[cite: 608]. Main components include:

* **Central Processing Unit (CPU):** Plays a key role in program running and data processing[cite: 609].
* **Memory:** Main memory (temporary, high speed) and auxiliary storage (secondary, low speed, mechanical devices)[cite: 610].
* **I/O device:** Input and output devices for interaction[cite: 610].

#### B) Types of Computer Architecture

1.  **Von Neumann architecture:** Applies the stored-program design principle; instructions and data both use the same memory/bus[cite: 611]. Read commands and write data are executed simultaneously because they use the same bus[cite: 612].
2.  **Harvard architecture:** Separates instruction memory and data memory[cite: 613]. Improves performance by reading and writing commands in parallel, solving computer bottlenecks[cite: 613].

### IV.02 CPU

#### A) Definition of CPU

The CPU is the most important part of computers, interpreting instructions and handling arithmetic/logical operations and data processing[cite: 614].

#### B) CPU Execution

The CPU operation is divided into execution steps:
* Instruction fetch [cite: 615]
* Instruction decoding [cite: 616]
* Data fetch/processing/storage [cite: 616]

#### C) CPU Components

The CPU consists of a control unit, an arithmetic logic unit (ALU), registers, and buses[cite: 617].

* **Control unit:** Sequentially generates control signals to interpret and run program codes (instructions)[cite: 618].
* **ALU (Arithmetic Logic Unit):** Executes arithmetic and logical operations[cite: 618].
* **Register:** Temporary storage area for instructions and intermediate results[cite: 619].
    * **Types:** PC (program counter), IR (instruction register), AC (accumulator), MAR (memory address register), MBR (memory buffer register), SP (stack pointer)[cite: 620].
* **Bus:** Transmission lines for address data (**Address bus**), data transfer (**Data bus**), and control signals (**Control bus**)[cite: 621].

#### D) Instruction Cycle

The entire process required for the CPU to execute an instruction[cite: 622]. It consists of four parts:

1.  **Fetch cycle:** Fetches an instruction from memory[cite: 623].
    * **Related CPU Components:** PC, MAR, MBR, and IR[cite: 623].
2.  **Indirect cycle:** Reads the actual data address from the memory unit[cite: 624].
3.  **Execution cycle:** Decodes the instruction and performs the needed operation[cite: 625].
    * **Related CPU Components:** AC, ALU, and Control unit[cite: 625].
4.  **Interrupt cycle:** Inspects the interrupt request signal, stores the current PC data in the stack, and loads the ISA's beginning address[cite: 626].

#### E) Instruction Set Structure, CISC and RISC

| Feature | CISC (Complex Instruction Set Computer) | RISC (Reduced Instruction Set Computer) |
| :--- | :--- | :--- |
| **Instruction Type** | Many complex instructions embedded into hardware[cite: 627]. | Few simple instructions embedded into hardware[cite: 629]. |
| **Control Type** | Micro-program type control[cite: 628]. | Hard-wired type control[cite: 630]. |
| **Compiler** | Simple compiler[cite: 628]. | Complex compiler[cite: 630]. |
| **Registers** | Few registers[cite: 628]. | Many registers[cite: 630]. |
| **Instruction Length** | Variable instruction length[cite: 628]. | Fixed instruction length (e.g., 32 bits)[cite: 630]. |
| **Example** | Intel series (x86)[cite: 628]. | ARM and MIPS[cite: 630]. |

### IV.03 Memory

#### A) Memory Unit's Hierarchical Structure

Memory is organized hierarchically[cite: 631].

| Level (Highest to Lowest) | Price per Bit | Capacity | Access Time | Access Frequency by CPU |
| :--- | :--- | :--- | :--- | :--- |
| **Register** | Higher [cite: 631] | Lower [cite: 631] | Shorter [cite: 631] | Higher [cite: 631] |
| **Cache Memory** | | | | |
| **Main Memory** | | | | |
| **Auxiliary Memory** | | | | |

* **Hierarchy:** Register, Cache Memory, Main Memory, Auxiliary Memory[cite: 632].

#### B) Factors for Performance Evaluation

* Capacity, access time, cycle time, bandwidth of storage unit, data transportation, and cost[cite: 633].

#### E) Locality

The tendency for programs to intensively refer to a specific area in memory[cite: 634].

* **Temporal locality:** Recently accessed programs/data are likely to be accessed again soon[cite: 635].
* **Spatial locality:** Data stored adjacent to storage is likely to be accessed continuously[cite: 636].
* **Sequential locality:** Instructions are fetched and executed in order (about 20%)[cite: 637].

### IV.04 I/O Device

#### A) Concept of I/O Device

A device necessary for input (storing data to be processed by the CPU) and output (transferring processing results from main memory)[cite: 638].

#### C) DMA (Direct Memory Access)

* **Concept:** A method where the I/O device directly accesses the memory without the assistance of the CPU[cite: 639]. The DMA controller handles the bus, and the I/O device handles memory transfer information[cite: 640].
* **Purpose:** Increases system efficiency for high-speed I/O devices by minimizing the interruption overhead[cite: 641].

**DMA Operation Mode**
1.  **Cycle stealing:** The fast CPU gives the slow DMA the priority of using the bus to enable fast inputs and outputs[cite: 642]. Applied when transferring data of about one word[cite: 643].
2.  **Burst mode:** Applied when transferring data in blocks[cite: 644]. Applicable to high-speed I/O devices[cite: 644].

### IV.05 Latest Technologies and Trends

* **Neuromorphic chip:** A new semiconductor type that processes information similar to human thinking by implementing brain behavior in silicon[cite: 645].
    * **Structure:** Employs several cores in a chip, with transistors and memory embedded into the core[cite: 646].
    * **Data Processing:** Performs parallel and integrated processing[cite: 648].
* **Quantum computer:** A new conceptual computer that can simultaneously process a large volume of information at high speed[cite: 649].
    * **Basic Unit:** Uses the quantum bit (**qubit**) as its basic unit of information processing[cite: 650].

---

## V. Data Processing Technology

This section covers technologies for high-performance and large-scale data processing, including parallel processing, storage technologies, disk scheduling, RAID, and graphic compression[cite: 652, 654].

### V.01 Parallel Processing System

* **Parallel Processing:** One or more independent operating systems managing multiple processors and performing multiple tasks simultaneously[cite: 655].

#### B) Flynn's Classification

| Classification | Description |
| :--- | :--- |
| **SISD** (Single Instruction Stream Single Data Stream) | Conventional computer architecture (Von Neumann)[cite: 656]. |
| **SIMD** (Single Instruction Stream Multiple Data Stream) | Processing multiple data with a single instruction simultaneously[cite: 657]. |
| **MISD** (Multiple Instruction Stream Single Data Stream) | Each processing unit runs different instructions and processes the same data; not widely used[cite: 658]. |
| **MIMD** (Multiple Instruction Stream Multiple Data Stream) | Multiple processors process different programs and data (most computers fall into this category)[cite: 659]. |

#### C) Classification by Memory Structure

| Classification | Coupling Type | Memory Usage | Scalability | Programming Ease |
| :--- | :--- | :--- | :--- | :--- |
| **SMP** (Symmetric multiprocessor) | Tightly-coupled [cite: 660] | All processors use shared main memory[cite: 661]. | Poor (due to bus bottleneck)[cite: 661]. | Easy to program[cite: 661]. |
| **MPP** (Massive parallel processor) | Loosely coupled [cite: 662] | Each processor has independent memory and exchanges data via a network[cite: 662]. | High[cite: 662]. | |
| **NUMA** (Non uniform memory access) | Combines with SMP [cite: 663] | Shared memory[cite: 663]. | Excellent[cite: 663]. | Easier development[cite: 663]. |

#### D) Types of Parallel Processor Technology

1.  **Instruction pipelining:** Improves CPU performance by dividing an operation into stages[cite: 664].
    * **Example:** Four-stage pipeline (Instruction Fetch (IF), Instruction Decoding (ID), Operand Fetching (OF), and Execution (EX))[cite: 665].
2.  **Superscalar process:** Allows execution of a number of instruction pipelines simultaneously using multiple pipelines[cite: 666].

#### E) Parallel Programming Technology

* **OpenMP (Open Multi-Processing):** A compiler directive-based parallel programming API[cite: 667]. Uses the fork/join model where a master thread creates and executes threads[cite: 668].
* **MPI (Message passing parallel programming model):** Suitable for a distributed memory system[cite: 669]. Nodes share information by transferring messages over the network[cite: 669].

#### G) GPU-based Parallel Programming Technology

* **CUDA (Compute Unified Device Architecture):** A parallel computing platform developed by NVIDIA for GPU development[cite: 670].
* **Open Computing Language (OpenCL):** An open, general-purpose parallel computing framework developed by Apple, IBM, Intel, and NVIDIA[cite: 671].

### V.02 Storage Technology

#### B) Connection of Storage Unit and Server

| Type | Connection Method | Key Characteristics |
| :--- | :--- | :--- |
| **DAS** (Direct attached storage) | Connected directly to the computer system (server) via a fiber channel or SCSI cable[cite: 672]. | Low cost, simple, high speed[cite: 672]. |
| **NAS** (Network attached storage) | Connected to a computer system through an Ethernet network interface (LAN or WAN)[cite: 673]. | Managed by a separate file system management server, easy to manage/share data[cite: 674]. |
| **SAN** (Storage area network) | Uses a dedicated fiber channel switch to provide a fast connection between connected servers and storage[cite: 675]. | Enables scaling up the number of connected servers/storage[cite: 675]. |

#### C) IP-SAN

Uses gigabit Ethernet Internet protocol (IP) instead of a fiber channel[cite: 676].
* **Types:** FCIP (Fiber Channel over IP), iFCP, and iSCSI[cite: 677].
* **iSCSI:** Encapsulates SCSI commands into IP packets for transfer and reduces network storage implementation cost[cite: 677].

#### D) Storage Capacity Management

* **Thin provisioning:** A storage virtualization technology that allocates data by mapping actual data space into a thin LUN (Logical Unit Number)[cite: 678].

#### E) Storage Disk Scheduling

* **Purpose:** To efficiently process I/O requests[cite: 679]. Goal: Maximization of throughput and minimization of response time[cite: 680].

**Scheduling Techniques (Examples)**

| Technique | Method | Advantages/Disadvantages |
| :--- | :--- | :--- |
| **FCFS** (First Come First Serve) | Serves requests in the order they are received[cite: 681]. | Simple, but movement may be inefficient[cite: 681]. |
| **SSTF** (Shortest Seeking Time First) | Serves requests closest to the current head position[cite: 682]. | Minimizes head movement, maximizes service response rate. Can cause starvation[cite: 683]. |
| **SCAN** (Elevator algorithm) | Serves all requests in one direction until reaching the end of the cylinder, then reverses[cite: 684]. | |
| **C-SCAN** (Circular SCAN) | Moves the head in one direction only; when it reaches the end, it moves to the initial position without serving requests[cite: 685]. | |

### V.03 High Availability Storage

#### A) Redundant Array of Independent Disks (RAID) Technology

RAID improves reliability, capacity, and speed by arranging storage devices in an array[cite: 686].

| RAID Level | Description | Key Characteristics |
| :--- | :--- | :--- |
| **RAID-0** | Striped disk array without fault tolerance[cite: 687]. | No redundancy; I/O speed is excellent[cite: 687]. |
| **RAID-1** | Mirroring and Duplexing (redundantly stores data on two drives)[cite: 688]. | Data redundancy; reduces reading performance somewhat, writing is slow[cite: 689]. |
| **RAID-5** | Parity across disks (distributes the load of the drive that stores the parity)[cite: 690]. | Requires at least three drives; highly effective in cost and performance[cite: 690]. |
| **RAID-6** | Stripe with dual distributed parity[cite: 691]. | Stores two parity bits, increasing redundancy over RAID-5[cite: 691]. |
| **RAID-10** | Striping & Mirroring (Combination of RAID-0 and RAID-1)[cite: 692]. | Requires at least four drives[cite: 692]. |

#### B) Backup Storage: LTO and VTL

* **LTO (Linear tape-open):** A standard open tape drive technology supporting high-speed data processing and large capacity[cite: 693].
* **VTL (Virtual tape library):** A backup solution that emulates disk storage into a virtual tape device to compensate for tape problems[cite: 694].

### V.04 Graphic Compression Technology

#### A) Graphic Compression Type

| Type | Description | Techniques |
| :--- | :--- | :--- |
| **Lossless compression** | Preserves the original data integrity (no loss)[cite: 695]. | Run-length encoding (RLE), dictionary coding, Huffman coding, and arithmetic coding[cite: 696]. |
| **Lossy compression** | Compresses data by allowing the loss of redundant or unnecessary data[cite: 697]. | Prediction coding and transformation coding (e.g., JPEG uses DCT)[cite: 698]. |

#### B) Multimedia Data

* **MPEG (Moving Picture Experts Group):** An international standardization organization that officially defines compression formats and standards[cite: 699].
    * **MPEG-1:** Audio and video compression (used for MP3 and video CD)[cite: 700].
    * **MPEG-2:** Compression for DTV (Digital TV and DVD)[cite: 700].
    * **MPEG-4:** Mobile phone video compression[cite: 701].
* **AVC codec (H.264):** Video compression technology jointly proposed by the ITU-T and ISO[cite: 702]. HEVC is the standard name for H.264[cite: 702].

---

## VI. Embedded System

An embedded system is a computer system designed to perform a specific function for controlling a machine or electronic device, configured with hardware and specialized software[cite: 704].

### VI.01 Overview of Embedded System

* **Embedded System:** A computer system that performs a specific function for controlling a machine or other electronic device[cite: 706].
* **Configuration:** Consists of **Embedded Hardware** (CPU, memory, I/O device, network device) and **Embedded Software** (OS and application software)[cite: 707].

#### B) Characteristics of Embedded System

* **Low cost:** Mass-produced, often using a relatively slow processor and small memory[cite: 708].
* **Low performance:** Usually slow due to the design goal of reduced size and cost[cite: 709].
* **Stability:** Designed to run reliably without error for many years (firmware goes through stringent testing)[cite: 710].
* **Resilience:** Applied in places difficult for humans to access[cite: 711]. Often includes a watchdog timer for emergency recovery[cite: 711].
* **Resource constraints:** Operates with limited hardware resources (no disk drive, limited memory)[cite: 712].

#### C) Embedded System Development Process

The development includes a hardware development process[cite: 713]. Stages involve:

1.  Product planning (commercial feasibility determination, specifications)[cite: 714].
2.  Part selection (hardware parts, OS/software specifications)[cite: 714].
3.  Hardware circuit generation and software structure design[cite: 715].
4.  Code design for each artwork module[cite: 715].
5.  Making the PWB (printed wiring board) and installing modules[cite: 716].
6.  Part mounting and hardware testing[cite: 716].
7.  Integrated testing and debugging[cite: 717].
8.  Mass-production testing[cite: 717].
9.  Quality inspection[cite: 717].
10. Specification inspection such as EMI and safety[cite: 717].
11. Product shipment[cite: 717].

### VI.02 Embedded Hardware

#### A) Microprocessor, the Key to Embedded Systems

* **Microprocessor Unit (MPU):** Performs arithmetic/logical operations and data storage[cite: 718].
    * **Types:** ARM, PowerPC, MIPS series. ARM CPUs are widely used[cite: 719].

#### B) Technical Trends of Embedded Hardware

* **Expanded connectivity:** Studies applying WIFI, LTE, BLE, and ZigBee[cite: 720].
* **Low-power 32-bit processor:** Processors for embedded systems are transitioning from 8 bits to 32 bits[cite: 721].
* **Polarization of lightweight/general-purpose OS:** Systems require lighter power consumption, enabling complex operations applied to 3D acceleration GUI and multimedia[cite: 722].

### VI.03 Embedded Software

* **Embedded Software:** Software installed in embedded systems[cite: 723].
    * **Classification:** Basic embedded application, embedded middleware (JVM, CORBA), embedded system software (Embedded OS, device driver)[cite: 724].

#### B) Characteristics of Embedded Software

* **Reactivity:** Continuously interacts with physical environmental changes by converting input data into output data at a specified speed[cite: 725].
* **Timeliness:** Time to convert input data into output data must be within a very short allowable range[cite: 726].
* **Concurrency:** Able to process input data generated by concurrent physical environmental changes[cite: 727].
* **Heterogeneity:** Effectively processes data from hardware or software[cite: 728].
* **Liveness:** Should never stop its operation, even after unexpected events[cite: 728].
* **Resource and environmental constraints:** Must meet the resource (CPU speed, memory size, I/O interface) and environmental constraints[cite: 729].

### VI.04 Embedded OS

* **Embedded OS:** An operating system optimized to execute application programs running on an embedded system with a built-in microprocessor[cite: 730].

#### B) Embedded OS Structure

The embedded OS has a structure supporting stable execution with a low-specification processor, limited memory, and storage space[cite: 731].

#### C) Types and Trends of Embedded OS

1.  **RTOS (Real Time OS):** Focuses on controlling application programs or hardware affected by a limited amount of time[cite: 733].
    * **Examples:** VxWorks, VRTX, QNX, pSOS[cite: 734].
2.  **Non-real time OS:** Focuses on development convenience, scalability, and diverse operating environments[cite: 734].
    * **Examples:** Linux series, embedded Windows XP, Windows CE[cite: 734].
* **Trends:** Linux is the leading OS, with Embedded Linux having the highest usage rate (22%)[cite: 735].

---

## VII. Information System Implementation

This section details the implementation of information systems, focusing on system structure (hardware, software, middleware) and the critical process of capacity calculation (sizing)[cite: 737]. It also covers modern infrastructure trends like Hyper-Converged Infrastructure (HCI)[cite: 737].

### VII.01 Information System Structure

* **Information System:** Uses IT to perform business procedures, requires necessary information, and creates a system that enables IT personnel to provide IT services[cite: 738].
* **IT Infrastructure Components:** Networks, hardware, software, IT personnel, and IT services[cite: 739].

#### B) Information System Structure

Information systems are generally composed of a 3-tier web system architecture or a client-server system[cite: 740]. The system is divided into physical areas (hardware) and program areas (software)[cite: 741].

**1. Information System Hardware Structure (Physical Domain)** [cite: 742]

| Classification by Performance | Classification by Configuration |
| :--- | :--- |
| **Entry server** (1-2 CPUs) [cite: 742] | **Rack-mount server** (fits into a rack) [cite: 743] |
| **Middle-range server** (4 or more CPUs, high-end servers) [cite: 742] | **Tower server** (in-house server room) [cite: 743] |
| **High-end server** (tens of millions of won, enterprise server) [cite: 742] | **Blade server** (multiple CPU blades in a box, small size) [cite: 743] |

**2. Information System Software Structure (Program Domain)** [cite: 744]

* **OS:** System software that operates and manages applications (e.g., Linux, UNIX, Solaris)[cite: 744].
* **Webserver:** Provides media content through the HTTP protocol[cite: 745]. Leading products include Apache, Nginx, and IIS[cite: 745].
* **Web application server (WAS):** Middleware enabling stable transaction processing of web client requests[cite: 746]. Handles database queries or business logic[cite: 747]. Leading products include Tomcat, JBoss, WebLogic[cite: 747].
* **Transaction processing (TP) monitor:** Middleware that supports distributed transaction processing[cite: 748]. Leading products include Tmax and Tuxedo[cite: 748].
* **DB server:** Provides database type, management technology, and query language[cite: 749].

### VII.02 Information System Capacity Calculation

* **System Sizing (Capacity calculation):** Estimating/calculating a system's size using a mathematical methodology, based on actual work and applications[cite: 750].

#### B) Size Calculation Targets

Targets generally include hardware and network components[cite: 751].

* **CPU:** Calculates the CPU size needed to process necessary tasks and achieve adequate performance[cite: 752].
* **Memory:** Calculates memory usage by software and applications based on server configuration[cite: 753].
* **Disk/Storage:** Calculates disk size by target system type (OLTP, Web/WAS) and the needed storage size according to the CPU type[cite: 754].

#### D) Size Calculation Procedure

1.  Implementation direction and reference data investigation[cite: 755].
2.  Basic data and task analysis[cite: 755].
3.  Reference model determination and server size calculation[cite: 756].
    * **Reference Model 1 (1-Tier):** Web, application, and database layers exist in a single server[cite: 756].
    * **Reference Model 3 (3-Tier):** Web layer on Server 1, application layer on Server 2, and database layer on Server 3[cite: 756].
4.  Application of weight factor for each reference model[cite: 757].

### VII.03 Latest Technology and Trends of Information Systems

* **Converged Infrastructure (CI):** Integrates hardware components (servers, storage, network) and software into single SKUs[cite: 758].
* **Hyper-Converged Infrastructure (HCI):** A newer type of integrated system that eliminates the limitations of CI[cite: 759]. HCI groups the direct attached storage (DAS) and uses software-defined storage (SDS) technology through an IP-based network[cite: 759].

---

## VIII. Fault Response Technology

Fault response technology ensures system service continuity despite failures[cite: 761]. Key concepts are High Availability (HA) and Disaster Recovery System (DRS)[cite: 762].

### VIII.01 High Availability (HA)

* **Concept of HA:** Refers to an uninterrupted service[cite: 764]. Requires configuring two or more systems using redundancy[cite: 764].
* **Availability (A) Calculation Formula:** $A=\frac{\text{MTBF}}{(\text{MTBF}+\text{MTTR})}$ (MTBF: Mean Time Between System Failures, MTTR: Time to Restore)[cite: 765].

| HA Configuration Type | Description | State of Servers |
| :--- | :--- | :--- |
| **Hot standby** | An active server and a standby server are used[cite: 766]. Service switches to the standby server upon active server failure[cite: 767]. | Active-standby [cite: 766] |
| **Mutual takeover** | Two or more operating systems run on separate servers[cite: 768]. Services switch to the designated server upon failure[cite: 768]. | Active-active [cite: 768] |
| **Concurrent access** | Multiple systems process tasks in parallel to provide availability[cite: 769]. | All servers operate in an active state[cite: 769]. |

### VIII.02 Fault-Tolerant System

* **Fault-tolerant system:** Can continuously perform functions even if a component fails[cite: 770].
* **Hardware tolerant technique examples:** Triple modular redundancy, RAID (through disk mirroring and distributed storage of parity bits)[cite: 771].
* **Software tolerant technique examples:** Checkpoint, Recover block, Conversation, Distributed rollback[cite: 772].

### VIII.03 Disaster Recovery System (DRS)

* **Definition of DRS:** An overall plan to minimize the impact of a disaster by locating all or part of the information system infrastructure in a remote location[cite: 773].

#### DR Center Types

| DR Center Type | RTO (Recovery Time Objective) [cite: 778] | State / Details |
| :--- | :--- | :--- |
| **Mirrored site** | Immediate [cite: 774] | Real-time simultaneous services in active-active state[cite: 774]. |
| **Hot site** | Within 4 hours [cite: 775] | Active/standby state, synchronous/asynchronous real-time mirroring[cite: 775]. |
| **Warm site** | Days - weeks [cite: 776] | Transferring critical components to the DR center[cite: 776]. |
| **Cold site** | Weeks - months [cite: 777] | Only keeping minimal resources[cite: 777]. |

* **Disaster recovery goal:** Measured by RTO and RPO[cite: 778].
    * **RPO (Recovery Point Objective):** Data loss converted into time at the time of disaster[cite: 778].
    * **RTO (Recovery Time Objective):** Maximum time allowed to downtime[cite: 778].

---

## IX. Cloud Computing Technology

Cloud computing provides on-demand IT resources over the Internet, emphasizing virtualization, immediacy, and linear scalability[cite: 780].

### IX.01 Definition of Cloud Computing

* **Cloud Computing:** A computing environment that uses IT resources over the Internet, based on virtualization and distributed processing[cite: 782].
    * **Benefits:** Reduced CAPEX/OPEX, reduced development time/risk, improved efficiency/resource usage, better product integration[cite: 783].
* **Comparison to Grid Computing:** Grid Computing is scattered and managed by different organizations (heterogeneous), while Cloud Computing is scattered but managed by a central organization (mostly same model)[cite: 784].

### IX.02 Cloud Computing Types

#### A) Classification According to the Service Type

| Service Type | Description | Example |
| :--- | :--- | :--- |
| **IaaS** (Infrastructure as a Service) | Provides infrastructure resources (server, storage, network)[cite: 785]. Can provide non-virtualized physical infrastructure (bare-metal cloud)[cite: 786]. | |
| **PaaS** (Platform as a Service) | Provides infrastructure, runtime, development/operation environment[cite: 787]. | A user developing a new Java web application using MySQL as a database[cite: 787]. |
| **SaaS** (Software as a Service) | Provides software and a model that delivers software serviced from the center to users[cite: 788]. | Google Docs and Salesforce.com[cite: 789]. |

#### B) Classification According to the Cloud Operation Form

* **Public cloud:** Cloud services disclosed to unspecified masses over the Internet[cite: 790].
* **Private cloud:** Cloud services implemented over the closed network by enterprises[cite: 791].
* **Hybrid cloud:** Services using both public and private cloud services[cite: 792].

### IX.03 Server Virtualization Technology

* **Virtualization:** Technology of abstracting computer resources of multiple computers to make them look like servers (or abstracting resources to make one computer look like multiple machines)[cite: 793].

#### A) Hypervisor

* **Hypervisor (Virtual Machine Monitor, VMM):** A technology of virtualizing a physical server[cite: 794]. It is a logical platform for server virtualization[cite: 794].

#### B) Hypervisor Types

1.  **Native type (Type 1):** Installs a VMM on physical hardware and requires no host OS[cite: 795].
    * **Example:** Xen, Hyper-V, KVM[cite: 795].
2.  **Hosted type (Type 2):** Software installed on an existing OS[cite: 796].
    * **Example:** VirtualPC, VirtualBox[cite: 796].

#### C) Server Virtualization Methods

1.  **Full virtualization:** Completely virtualizes the hardware[cite: 797]. The guest OS perceives that it owns and accesses the hardware directly[cite: 797]. No restrictions on the guest OS[cite: 798].
2.  **Para-virtualization:** Does not completely virtualize the hardware[cite: 799]. Uses a hypervisor API to access hardware resources[cite: 799].
3.  **OS-level virtualization (Container virtualization):** Uses the virtualization technology included in the OS, instead of a hypervisor[cite: 800].
    * **Advantages:** Quick start, minimized resource consumption, low overhead[cite: 801].
    * **Disadvantage:** Host OS dependent; cannot configure the kernel for each container[cite: 801].
    * **Example:** Solaris Containers, Linux Containers (LXC), Docker[cite: 802].

### IX.05 Cloud Platform

* **Cloud platform:** A cloud operation system to collect, control, and operate resources[cite: 803].
    * **OpenStack:** Open-source project for building public/private cloud computing platforms[cite: 804].
    * **Kubernetes:** An orchestration platform for container management and operation[cite: 805].
    * **Mesos:** A resource management project that enables integrated management of cloud infrastructure resources[cite: 806].

---

## X. Big Data System

This section focuses on the Big Data System (BDS) architecture, particularly the Hadoop ecosystem[cite: 807].

### X.01 Big Data System Structure

#### A) Hadoop Ecosystem

* **Hadoop:** A Java-based framework for the distributed processing of a large volume of data in multiple distributed storage[cite: 809]. It uses HDFS (Hadoop Distributed File System) and MapReduce[cite: 809].

#### B) Hadoop's Main Technology Elements

1.  **HDFS (Hadoop distributed file system):** A distributed file system that stores data in devices connected to the Hadoop network[cite: 810].
    * **Characteristics:** Prevents data loss by storing replicated data in multiple nodes[cite: 811]. Ensures data integrity (Version 2.0 or higher allows appending to the saved file)[cite: 812].
    * **Architecture:** Consists of one **NameNode** (server managing all metadata) and multiple **DataNodes** (servers storing the blocks)[cite: 813].
2.  **MapReduce:** A programming model and software framework for processing a large volume of data[cite: 814].
    * **Map:** Classifies scattered data into relevant data (key or value type)[cite: 815].
    * **Reduce:** Removes duplicate data and extracts the desired data[cite: 816].

#### C) Hadoop Support Program

| Type | Program Examples | Description |
| :--- | :--- | :--- |
| **Streaming data collection** | Flume, Scribe, Chuckwa[cite: 817]. | |
| **Structured data collection** | Sqoop, Hiho[cite: 818]. | |
| **Distributed database** | Hbase, Cassandra[cite: 818]. | Hbase is a Hadoop-based column-based NoSQL database[cite: 818]. |
| **Real-time query** | Impala[cite: 819]. | Hadoop-based real-time SQL query system[cite: 819]. |
| **Metadata management** | HCatalog[cite: 820]. | |
| **Data analysis** | Hive, Pig[cite: 820]. | Hive is similar to SQL-based processing; Pig provides a proprietary language (Pig Latin)[cite: 820]. |

---

## XI. Datalink Layer

The Datalink Layer (Layer 2 of OSI) is responsible for transferring data between peripheral devices using the physical layer[cite: 821]. This layer handles encapsulation, MAC address allocation, and error detection/correction[cite: 822].

### XI.01 Concept of Datalink Layer

* **Datalink Layer:** Transfers data between peripheral devices on the network using the physical layer[cite: 823]. It ensures devices receive signals properly and detects/corrects errors in transmitted signals[cite: 824].

### XI.02 Encapsulation of the Datalink Layer

* **Encapsulation:** The datalink layer frame adds a header and a trailer to the network layer packet[cite: 825]. The reverse is called decapsulation[cite: 826].
* **Frame header and trailer:** The header includes a preamble for bit synchronization, and the trailer includes a frame check sequence (FCS) to check for errors[cite: 827].

### XI.03 Datalink Layer Configuration

The datalink layer consists of two sub-layers: **LLC (Logical Link Control)** and **MAC (Media Access Control)**[cite: 828].

#### B) Logical Link Control (LLC)

* **Role:** Responsible for data transfer between two adjacent nodes, using DSAP and SSAP on the network layer[cite: 830].
* **LLC options:** Type 1 (unconfirmed datagram), Type 2 (connection-oriented, like TCP), Type 3 (confirmed datagram)[cite: 831].

#### C) MAC

* **MAC sub-layer:** Responsible for determining how to transfer data through physical media[cite: 832]. Includes the **MAC address** (48-bit unique system)[cite: 833].

### XI.05 Techniques of Datalink Layer Error Detection and Correction

#### A) Concept of Error Control

* **Error Control:** The function of guaranteeing data transmission integrity[cite: 834].
* **FEC (Forward Error Correction):** The receiving device detects and corrects errors by transmitting a spare bit[cite: 835].
* **BEC (Backward Error Correction):** Notifies the transmitting device to recover from the error[cite: 836].

#### B) Error Detection and Correction Methods

| Method Type | Techniques | Description |
| :--- | :--- | :--- |
| **Error detection methods** (Use redundancy) [cite: 837] | VRC (Vertical Redundancy Check) [cite: 838] | Most widely used, includes parity check[cite: 838]. |
| | LRC (Longitudinal Redundancy Check) [cite: 839] | Collecting the even parity of all bytes[cite: 839]. |
| | CRC (Cyclic Redundancy Check) [cite: 840] | Detection method using binary division[cite: 840]. |
| | Checksum [cite: 841] | Used by higher-level protocols[cite: 841]. |
| **Error correction methods** | Single bit error correction [cite: 842] | Uses the principle of error correction to locate the wrong bit, called a parity bit[cite: 842]. |
| | Redundant error correction [cite: 843] | Adjusting the relationship between data bits and redundant bits[cite: 843]. |
| | Hamming code [cite: 843] | Finding the redundant bit position[cite: 843]. |
| **Automatic repeat request (ARQ)** | Stop-and-wait ARQ, Go-back-N ARQ, Selective-repeat ARQ, Adaptive ARQ[cite: 844]. | Receiving side informs sending side of error; sending side retransmits the frame[cite: 844]. |

### XI.06 IEEE 802 Standard

The IEEE 802 defines services for each layer adjoining the LLC sub-layer[cite: 846].

* **IEEE 802.3 standard:** Corresponds to the LLC layer and MAC layer that includes Ethernet, token ring, and FDDI[cite: 847].
* **IEEE 802.11 standard (Wi-Fi):** Wireless communication standardization committee for wireless LAN[cite: 848]. Uses DSSS modulation[cite: 848].
* **IEEE 802.15 standard:** Short-range wireless communication standardization committee[cite: 849].
    * **Types:** Bluetooth (voice/file transfer), UWB (multimedia), ZigBee (sensor communication)[cite: 850].

---

## XII. Network Layer

The Network Layer (Layer 3 of OSI) is responsible for efficient data transmission using IP-based packets[cite: 851]. This section covers network layer functions, internetworking equipment, routing, and IPv4/IPv6 addressing[cite: 852].

### XII.01 Network Layer Overview and Equipment

* **Network Layer:** The third layer of the OSI 7 model, sending packets from a transmitting side to a receiving side[cite: 853].
* **Network layer function:**
    * **Packetizing:** Encapsulating and decapsulating the payload[cite: 854].
    * **Routing:** Finding the optimal communication path to the destination[cite: 855].
    * **Forwarding:** Performs the action when a packet has arrived through an interface[cite: 856].

**Internetworking Equipment**
* **Repeater:** Device that enhances (amplifies or reproduces) signals[cite: 857].
* **Bridge:** Device that connects two LANs[cite: 857].
* **Switch:** Device that has the concept of a multi-port bridge (separates network based on MAC address)[cite: 858].
* **Router:** Device that finds the optimal communication path when connecting to a heterogeneous network[cite: 859].

* **VLAN (Virtual local area network):** A method of configuring a logical network, allowing users to overcome physical and regional constraints[cite: 860].

### XII.02 Network Layer Encapsulation

* **Network layer encapsulation:** Configures the packets by adding a header to the transmitting layer segment[cite: 861].
* **IPv4 header:** Includes Version, IHL, Type of Service, Total length, Identification, Flags, Fragment Offset, Time to Live (TTL), Protocol, Header Checksum, Source Address, and Destination Address[cite: 862].

### XII.03 Packet Switching and Network Layer Protocol/Instruction

* **Packet switching:** The method of finding the packet path in a packet-exchanging network[cite: 863].
* **Network layer protocols:**
    * **ARP** (Address Resolution Protocol): Converts an IP address into a MAC address[cite: 864].
    * **RARP** (Reverse Address Resolution Protocol): Converts a MAC address into an IP address[cite: 865].
    * **ICMP** (Internet Control Message Protocol): Reports error and control information[cite: 865].
    * **IGMP** (Internet Group Management Protocol): IP multicasting[cite: 866].

### XII.04 Network Service Quality (QoS)

* **Quality of Service (QoS):** Technology guaranteeing service quality and performance of communication service[cite: 867].
* **Attributes:** Confidence, Delay, Jitter, Bandwidth[cite: 867].
* **Quality implementation technique:**
    * **Scheduling:** FIFO, Priority, Weighted fair queuing[cite: 868].
    * **Traffic shaping/policing:** Leaky bucket, Token bucket[cite: 869].
    * **Service quality models:** Integrated service (IntServ) and Differentiated service (DiffServ)[cite: 870].

### XII.05 Routing Protocol Algorithm and Type

* **Routing algorithm:** Finds the low-cost path between a source router and a destination router in a graphical network[cite: 871].

#### Routing Algorithm Types

| Type | Description | Example Algorithm |
| :--- | :--- | :--- |
| **Link state routing** | Each router calculates the low-cost path to all destinations with the configuration and link-state information of the entire network[cite: 872]. | Dijkstra algorithm[cite: 872]. |
| **Distance vector routing** | Each router maintains the low-cost path table (vector) to all destination routers[cite: 873]. | Bellman-Ford algorithm[cite: 873]. |

#### Routing Protocol Types

| Type | Sub-Type | Protocol Examples | Usage |
| :--- | :--- | :--- | :--- |
| **Static Routing** | Fixed routing information[cite: 874]. | | |
| **Dynamic Routing** | **IGP** (Interior Gateway Protocol - Used within an AS) [cite: 875] | **Distance Vector:** RIP, IGRP[cite: 876]. **Link State:** OSPF, IS-IS[cite: 876]. | Within an Autonomous System (AS)[cite: 875]. |
| | **EGP** (Exterior Gateway Protocol - Used between ASs) [cite: 877] | BGP (Border Gateway Protocol)[cite: 877]. | Between ASs[cite: 877]. |

### XII.07 IPv4 Address Designation System and Subnetting

* **IPv4 address:** A 32-bit address[cite: 878].
* **IPv4 designation system (Classes):** Divided into Classes A, B, C, D (multicast), and E (experimental) based on the network size[cite: 879].
    * **Class A:** Network ID is first octet (1.0.0.0 ~ 126.255.255.255)[cite: 880].
    * **Class C:** Network ID is first three octets (192.0.0.0 ~ 223.255.255.255)[cite: 881].
* **Special IPv4 address:** Includes network address (0.0.0.0), limited broadcast (255.255.255.255), and private addresses (10., 172.16-31., 192.168.)[cite: 882].
* **Subnetting:** Dividing a given IP address into multiple smaller networks[cite: 883]. A subnet mask is used to separate the network address[cite: 884].
* **CIDR (Classless Inter-Domain Routing):** Combining multiple Class C addresses into a network to reduce routing table size and prevent wasted IP addresses[cite: 885].
* **Supernetting:** Opposite of subnetting, consolidating several small networks into one large network[cite: 886].
* **DHCP (Dynamic Host Configuration Protocol):** Protocol for dynamically allocating IP addresses, default gateway, and lease period[cite: 887].
* **NAT (Network Address Translation):** Connects internal network private addresses to external public networks[cite: 888].

### XII.08 IPv6 Overview

* **IPv6 (Internet Protocol Version 6):** The next-generation Internet protocol with a **128-bit** addressing system[cite: 889]. It provides security functions like address depletion solution[cite: 889].

### XII.09 IPv6 Addressing System and Header Structure

* **IPv6 addressing system:** 128 bit long, expressed in hexadecimal[cite: 890].
* **IPv6 header structure:** Includes Version, Traffic class, Flow Label, Payload length, Next Header, Hop Limit, Source Address, Destination Address[cite: 891].

---

## XIV. Transport Layer Protocol

The Transport Layer (Layer 4 of OSI) is responsible for end-to-end communication between hosts[cite: 892]. Major protocols are TCP (reliable), UDP (fast), and SCTP (combines advantages)[cite: 893].

### XIV.01 Concept of Transport Layer Protocol

* **Transport layer protocols:** Transmit application data between end-point hosts[cite: 895].
* **Major protocols:** TCP, UDP, and SCTP[cite: 895].

### XIV.02 TCP

#### A) Characteristics of TCP

* **TCP (Transmission Control Protocol):** A stream-based protocol providing connection establishment and reliable data transfer[cite: 896].
* **Reliability:** Achieved through techniques like sequence number and acknowledgment number check[cite: 897].
* **Flow control:** Controls the packet flow volume to prevent packet loss[cite: 898].
* **Error control:** Detects error codes, retransmitting lost packets[cite: 899].
* **Congestion control:** Occurs when network load reduces the number of packets transmitted[cite: 899].

#### B) Virtual TCP Operation Scenario

* **TCP connection setting (3-way handshake):**
    1.  Sender sends segment with **SYN** flag set[cite: 900].
    2.  Receiver sends segment with **SYN** and **ACK** flags set[cite: 901].
    3.  Sender sends segment with **ACK** flag set, establishing a bidirectional connection[cite: 902].
* **TCP connection termination:** Uses the **FIN** (Finish) segment[cite: 902].
* **Flow control:** Uses the **sliding window protocol**[cite: 903]. Maximum window size is 65,535 bytes[cite: 903].
* **Congestion control:** The **slow start algorithm** exponentially increases the congestion window size[cite: 904].

### XIV.03 UDP (User Datagram Protocol)

* **Characteristics of UDP:** A **connectionless service** for sending/receiving data without a pre-configuration process[cite: 905].
* **Details:** It is an independent datagram and does not assign a sequence number; error/flow/congestion control generally does not occur[cite: 906].
* **Usage:** Used for video play, voice transmission, multicast communication[cite: 907].

### XIV.04 SCTP (Stream Control Transmission Protocol)

* **Characteristics of SCTP:** A new transport layer protocol combining UDP and TCP advantages[cite: 908].
    * **Features:** Process-to-process communication, multi-stream service, allowed connection on each terminal[cite: 909]. Supports multi-homing[cite: 909].
    * **Reliability:** Connection-oriented and uses acknowledgment to confirm data arrival[cite: 909].

---

## XV. Application Layer Technologies, Including Web Application

The Application Layer (Layer 7 of OSI) provides network application services and protocols[cite: 911].

### XV.01 What is Application Layer Protocol?

* **Application Layer Protocol:** Protocols used to exchange necessary information between application programs[cite: 913].
* **Examples:** FTP, Telnet, SMTP, POP3, IMAP4, HTTP[cite: 913].

### XV.02 HTTP

* **HTTP (Hypertext Transfer Protocol):** An application layer protocol for hypermedia information systems that connects text, video, and audio files[cite: 914]. Used for transferring web contents since the early 1990s[cite: 914].
* **HTTP status codes:**
    * **200 (OK) or 206 (Partial Content):** Request processed successfully[cite: 915].
    * **Codes starting with 4 or 5:** Indicate client/server errors[cite: 916].
* **HTTP Methods:**
    * **GET:** Used mainly to search for content in the server[cite: 917].
    * **POST:** Used mainly to deliver user input information[cite: 917].

### XV.03 File Transfer Protocol

* **FTP (File Transfer Protocol):** A protocol for transferring a file or part of a file from one system to another[cite: 918]. Uses ports 21 (control connection) and 20 (data connection)[cite: 918].

#### Comparison of General Transfer Mode and Passive Transfer Mode

| Type | General Transfer Mode (Active) | Passive Transfer Mode |
| :--- | :--- | :--- |
| **Concept** | Data transfer by a server connecting to the client's specific port[cite: 919]. | Data transfer by a client connecting to the server's specific port[cite: 920]. |
| **Data Port** | Control port: 21, Data port: 20[cite: 920]. | Control port: 21, Data port: 1024 or higher[cite: 920]. |


