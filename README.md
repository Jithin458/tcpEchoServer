# TCP Echo Server (Winsock, C)

This project is a simple TCP Echo Server built using the Winsock API in C for Windows. It demonstrates the fundamentals of socket programming and networking at a low level.

##  What I Learned

- Basics of **Winsock** and how to initialize it with `WSAStartup()` and clean up with `WSACleanup()`
- Creating and managing **sockets** using `socket()`, `bind()`, `listen()`, and `accept()`
- Handling **client-server communication** using `send()` and `recv()`
- The difference between **Echo Servers** and **Chat Servers**
- Using `sockaddr_in` to represent IP address and port configurations
- Running C socket programs on Windows using `gcc` and linking with `-lws2_32`

## How It Works

The server:

1. Initializes Winsock.
2. Creates a TCP socket.
3. Binds to a specified port.
4. Listens for incoming client connections.
5. Accepts a client and receives messages.
6. Sends the same message back to the client (echoes it).
7. Closes the socket and cleans up Winsock.

##  How to Run (Windows)

Compile with GCC:

```bash
gcc server.c -o server.exe -lws2_32
```

Then run:

```bash
.\server.exe
```

Similarly, you can create a simple client (e.g., `client.c`) and compile it:

```bash
gcc client.c -o client.exe -lws2_32
.\client.exe
```

## Note

This project is for **learning purposes**. It's a foundational step toward understanding more advanced socket applications, like multi-client chat servers.



---



