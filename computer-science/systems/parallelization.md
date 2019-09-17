# Parallelization

## Deadlock

Locks acquired & waiting w/ no unlock  
Circular wait  
Avoided if you keep multiple lock access consistent in ordering \(L1 then L2...\)

## Heisenbugs

not deterministic, only show up sometimes, very hard to debug

### Performance

Bottlenecks hard to understand, waiting time hard to profile

### Load Balancing

### Processes

Message passing, how communication with processes works.

Processes don't share memory.

### Sockets

endpoints, udp/tcp

#### Serialization / Deserialization

Packing and unpacking memory into byte arrays to be sent, and rebuilt as the appropriate variable. Could also use formats like Google's Protobuffers.



