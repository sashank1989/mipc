# mipc
A multicast IPC framework for Minix developed as part of IIT's CS551 course

MINIX currently supports kernel IPCs that allows a sender to send a message to a receiver. 
In this project, we develop a set of IPC system calls that allow an application process to send messages to other application processes.

REQUIREMENTS :

1. At the heart of this set of IPC’s is a pair of msend and mreceive system calls. 
   A user process calls msend to send a message to a group of other user processes who call mreceive to retrieve the message. 

2. We require that messages from common senders will be delivered in the same order and in the same interleaving (receiver consistent). 
   A receiver is blocked on the call to mreceive if no message has yet been sent to it or if there is, it may violate receiver consistency. 

3. A process can belong to more than one group.
   
4. The other system calls(openGroup, closeGroup and recoverGroup) allow the programmer to setup, remove and to recover a multicast group from exception conditions respectively.

Project hosted privately at https://bitbucket.org/sashankbv/mipc

