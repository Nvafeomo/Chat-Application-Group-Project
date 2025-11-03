## Project Summary
This project implements a multi-client TCP chat server in C using POSIX sockets and pthreads. Developed as part of a group assignment, the server handles concurrent client connections, broadcasts messages, and manages thread-safe communication using mutexes.

The server was written and tested in a **Linux virtual machine** using Ubuntu. I wrote the server program and created a Java GUI, but we ended up not using it and went with C implemented GUI created by another group member. The server remains fully compatible with any standard TCP client.

---

##  Key Features
- Accepts up to **5 simultaneous clients**
- Uses **POSIX threads** for concurrent client handling
- Implements **mutex locking** to prevent race conditions
- Broadcasts messages from one client to all others
- Gracefully handles client disconnects and server capacity limits
- Sends a `-1` message to clients if the server is full

---

## Technologies Used
- **C** (POSIX sockets, pthreads)
- **Linux VM** for development and testing
- **VS Code** as the primary IDE

---

## Getting Started

###  Prerequisites
This server is designed for **Linux environments**. It will not compile on native Windows without significant modification.

Make sure you have:
- GCC compiler
- POSIX development headers

Install essentials:
```bash
sudo apt update
sudo apt install build-essential

### Compilation
**Compile Server**
gcc server.c -lpthread -o server
**Run Server**
sudo ./server or ./server 8080(specified port)
**Compile Client**
gcc client.c -o client

./client 8080(Specify port if applicable)

### Termination

Press Ctrl+C in the server terminal to shut down the program


