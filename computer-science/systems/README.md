# Systems

## Principal Types of Computing Systems

### Transactional

Needs caching, in the critical path of a waiting user

### Analytical

Huge data ingestion, no time pressure  


#### Idempotency

### Memory

#### Heirarchy

\(Not true everywhere, but most common\)

Disk &gt; RAM &gt; L3 Cache \(last level cache\) &gt; L2 Cache &gt; L1 Cache &gt; Register \(L0 Cache\)

RAM will be shared by processors

L3 on is single processor, multi-core

L2 on is single core, multi-cpu

Register is single CPU

#### Disk

#### RAM

#### Main Memory Bus

#### Caching

In terms of expense to going to the disk, or even a RAM memory bus, caching is orders of magnitude faster.

Why cache?

- temporal locality: recently used data likely to be reused

- spacial locality: nearby data to recently used is likely to be used

MESI

Cache sharing protocal, for modified, exclusive, shared, invalid  


#### Virtual Memory

#### Paging & Thrashing

#### Heap vs Stack

heaps global \(malloc, free, get pointers here\)

stacks local variables  


### Processing

Dennard's Scaling

Something to do with heat dissipation I think

Moore's Law

No longer valid after around 2020, that the density of processors would double every X years or so. We're now at physical barriers to optimize further  


#### SIMD & GPU's

single instruction multiple data processors \(gpu's, intel's Phi coprocessors\) great at linear algebra

#### CPU's

More general, more energy, &lt;&lt; more specific, less energy

CPU &lt;&lt; GPU/TPU &lt;&lt; FPGA &lt;&lt; ASIC  


Conditioning & Branching

speculation, throws away branches not taken  
  


### Parallelization

#### Concurrency

Multithreading

Hyperthreading

Multiprocessing

Embarrassingly Parallel Tasks

no coordination between tasks required at all, a good goal to strive for

Fault Tolerance

s

#### Atomicity & Isolation

#### Race Conditions

Locks, semaphores, mutexes

threads block each other, or you can YOLO it with some careful libraries

#### Map Reduce 

[Original Paper](https://drive.google.com/open?id=1Z0Y7_ZyBDYh_QLYqU4tl4kT37WN8UeQZ)

Distributed a list of key/value pairs to "map" an intermediate list of key/value pairs, and summarily "reduce" them down.  


Users specify a map function that processes a key/value pair to generate a set of intermediate key/value pairs, and a reduce function that merges all intermediate values associated with the same intermediate key.  


we designed a new abstraction that allows us to express the simple computations we were trying to perform but hides the messy details of parallelization, fault-tolerance, data distribution and load balancing in a library  


handles fault tolerance by pinging workers and marking for redos any tasks assigned to a non responsive worker.

toxic tasks are marked after multiple failed rescheduling

Apache Spark

Google's Jeff Dean's baby

Apache Spark is the open source version I gather  


### Information Retrieval

#### Web Crawlers

#### Search Engines

Inverted indices

### File Systems

Hadoop

Google's open sourced version of their proprietary file system  


