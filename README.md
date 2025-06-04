# Multithreaded-chat-application-java

Company - Codtech IT Solutions
Name - Tanay Daata
Inter Id - CT04DL566
Domain - Java Programming
Duration - 4 Weeks
Mentor -  Mr. Muzammil Ahmed

# 💬 Java Multithreaded Client-Server Chat Application

## 📌 Overview

This project is a **Client-Server Chat Application** built using **Java Sockets** and **Multithreading** to allow **multiple clients to communicate with a central server in real time**. It demonstrates the principles of concurrent programming, network communication, and socket-based messaging in Java.

The **deliverable** is a fully functional application where:

* The **server** accepts multiple client connections.
* Each **client** can send and receive messages.
* Messages are broadcast to all connected clients, simulating a group chat experience.

This application is ideal for students, hobbyists, and beginner backend developers learning about networking and concurrent programming in Java.

---

## ✅ Features

* 🌐 Real-time text chat system
* 🧵 Multithreaded server handles multiple clients simultaneously
* 💬 All client messages are broadcast to other users
* 🔒 Graceful client disconnection handling
* 🧹 Clean architecture using separate classes for server, client, and client handlers
* 🧠 Console-based user interface for simplicity

---

## 📁 Project Structure

```
ChatApp/
│
├── Server/
│   ├── Server.java              # Starts the server, listens for clients
│   └── ClientHandler.java       # Handles client threads
│
├── Client/
│   └── Client.java              # Connects to server, reads/writes messages
│
├── README.md                    # Documentation
└── .gitignore
```

---

## 🔧 Technologies Used

* **Java SE 8+**
* **java.net.Socket / ServerSocket**
* **java.io.BufferedReader, PrintWriter**
* **Multithreading with `Thread` and `Runnable`**

---

## ▶️ How to Run

### 1. Start the Server

Compile and run the server on your local machine:

```bash
javac Server/Server.java Server/ClientHandler.java
java Server.Server
```

### 2. Start Clients

Open multiple terminals and run:

```bash
javac Client/Client.java
java Client.Client
```

Each client connects to the server and starts chatting.

---

## 📌 Sample Output

### Server

```
[Server Started on port 1234]
[Client Connected: 127.0.0.1]
[Client Connected: 127.0.0.1]
```

### Client A

```
Enter your name: Alice
[Alice joined the chat]
Bob: Hello everyone!
Alice: Hi Bob!
```

### Client B

```
Enter your name: Bob
[Bob joined the chat]
Bob: Hello everyone!
Alice: Hi Bob!
```

---

## 🧠 Key Concepts Demonstrated

* **Sockets**: Create reliable TCP connections between server and clients.
* **Multithreading**: Server spins off a new thread for each client using `ClientHandler`.
* **Shared Resources**: Server manages a list of clients to broadcast messages.
* **I/O Streams**: Reads/writes messages using buffered input/output streams.
* **Concurrency**: Handles many clients at the same time without blocking.

---

## 📋 Error Handling

* Prevents server crash when a client disconnects unexpectedly.
* Validates empty or malformed input.
* Handles network exceptions gracefully with descriptive error messages.

---

## 🤓 Learning Outcomes

By building this application, you’ll understand:

* The basics of Java socket programming.
* How threads can be used to handle multiple connections.
* Synchronization concerns in concurrent applications.
* Efficient text-based data transmission between machines.

---

## 🚀 Possible Enhancements

* GUI using JavaFX or Swing
* Private (1-to-1) messaging support
* Message history logging
* Encryption for secure communication
* File sharing support between clients

---
