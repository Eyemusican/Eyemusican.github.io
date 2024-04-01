---
Title : DBS101 Flipped class 7
categories : [DBS201, Flipped_Class7]
tags : [DBS101]
---
## Database Storage Structures and Buffer Management
Hello there! Today, this seventh journal explores the concepts of disk block management, RAID configurations, and buffer pool management, which are fundamental components of database storage structures.

Not only that, it also covers building a simple relational database System from scratch, which I will explain after the components of database storage structures. Without any delay, let's get started.

---

###  disk block management
Disk blocks are the basic units used to store data on hard disks.. It is used to read a file or write data to a file.

![alt text](../21.png)

### RAID (Redundant Array of Independent Disks)
RAID (Redundant Array of Independent Disks) is a technology that combines multiple physical disk drives into a single logical unit, providing data redundancy and improved performance or is a way of storing the same data in different places on multiple hard disks or solid-state drives (SSDs). 
This is done in-order to protect data in the case of a drive failure. 

![alt text](../20.png)

The keyword for the RAID is:
1. stripping: sharing data across multiple disks
2. mirroring: duplicate the storage of data.


### Buffer Pool Management
A database buffer pool is a cache in a database management system (DBMS) that stores frequently accessed data in memory, allowing quicker access.

It is responsible for moving physical pages back and forth from main memory to disk. It allows a DBMS to support databases that are larger than the amount of memory that is available to the system

![alt text](../22.jpg)



## Building a Simple Relational Database System from scratch

Building a simple relational database system from scratch refers to the process of creating a basic database management system (DBMS) that can store, insert, deleted and retrieve data using the relational model. The relational model is a way of organizing data into tables (relations) with rows (records) and columns (attributes).


