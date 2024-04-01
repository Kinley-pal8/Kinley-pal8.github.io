---
Title: DBS101 Flipped Class 7
categories: [DBS101, Flipped_Class]
tags: [DBS101]
---

### Topic : Summary on Storage and Buffer management - Simulate disk blocks, RAID configurations, and buffer pools.

---

The guided task details three tasks related to storage and buffer management: simulating disk blocks, RAID configurations, and buffer pools. Here is a summary based on the tasks:

- Disk Block Implementation:
  It emulates a disc that supports a set number of tracks and block size.
  Techniques like assigning sequential blocks, file reading and writing, releasing the memory, and do the defragmentation fall under this category.
  It discusses blocks of data schemes as they appear on the disk every time data is written, read, allocated, and defragged.
  The summary on the code given:
    - Built a DiskBlock instance with 10 blocks of size 512 bytes.
    - Allocated contiguous blocks for data1 and read data to those blocks.
    - After deallocating data1, it allocated new blocks for data3.
    - Finally, It defragment the disk, which consolidates the allocated blocks for data3.

- RAID Configurations:
  It included RAID levels 0, 1 as well as 5 and with the appropriate block size as per operator/sysadmin requirement while number of disks is chosen as default settings.The head arranges striping, mirroring, and parity calculations according to the RAID level selected.
  It covered  the procedures for data rescuing, writing data over the faulty hard drive and rewriting it all on the spare drives.
  Demonstrated the activities: writing, reading the different drives, simulating the disk failure and rebuilding the system of RAID 0 and RAID 1 configurations.
  The summary on the code given:
    - It created a RAIDArray instance with 4 disks, block size 512 bytes, and RAID level 0 (striping).
    - It wrote data to the RAID 0 array and read it back.
    - It created another RAIDArray instance with 4 disks, block size 512 bytes, RAID level 1 (mirroring), and 1 spare disk.
    - It wrote data to the RAID 1 array, read it back, simulated a disk failure, and rebuilt the array using the spare disk.

- Buffer Pool Management:
  Introduced a database buffer pool in a DBMS that caches frequently accessed data pages in memory.
  Featured a BufferPool class with methods to fetch pages, track usage frequency, and manage the buffer pool.
  Demonstrated fetching pages, evicting the least recently used page when the buffer is full, and maintaining page content in the buffer pool.
  
At last, carrying/working on this practical helps to create an advanced understanding as well as model and ensure disk blocks, RAID configurations, and buffer pools are managed in a storage system.

---

The summary for the exercise:

According to the relevant materials given, the paper introduces chidb, a quarter-long C programming project of which is the students implement a basic relational database management system that is largely from scratch. The key components students build include:

File Format:
- Saves files having structures that are a part of the SQLite file format.
- Store a table as a B+-tree data structure, and index values as separate index B-tree.
- Websites use different types of pages, such as HTML, with cells storing nodes and collections of key-value pairs.

B-Tree Module:
- Exposes API to allows operations of creating, inserting and searching for B-trees.
- In the first assignment, students should demonstrate their understanding and use of this crucial module.

Database Virtual Machine (DVM):
- A virtual machine brand custom built to use with chidb database files.
- Has the 36 demand instructions like low-level making tables and high-level finding keys.
- Include them in registers, program counter (or cursors are equivalent).
- Second step is to put DVM into play.

SQL Compiler:
- SQL statements are translated to the relational algebra abstract syntax tree via the use of this tool.
- The code-generator transforms queries into DVM programs by stepping through the expression-tree.
- Transfer the third task to compose the generator code for basic requests.

Query Optimization:
- Fourth assignment coerces compiler to work with optimization stages.
- adopting indexes, talking show selections, punching before selections.


Thus, the architecture aims to mimic a real RDBMS while allowing students to focus on database concepts over low-level details. The assignments build up the full system in stages.The researchers have utilized chldb for 5 times of their database course for advanced students, while displaying satisfactory results in understanding internal detail of RDBMS. Such modification might include making concurrency control and better query optimization assignments. Bringing an open-source model to the classroom permits other teachers to be able to either expand or modify the chidb.  