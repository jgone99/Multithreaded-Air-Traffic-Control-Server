# Multithreaded Air Traffic Control Server

A concurrent network server written in C that simulates an air traffic ground control system. The server manages multiple airplane clients, coordinates takeoff sequencing, and ensures safe concurrent operations using synchronization primitives.

## Features

- Multithreaded client handling using POSIX threads
- TCP socket-based communication between server and clients
- Custom application-layer protocol for aircraft commands
- Thread-safe shared state using mutexes, read-write locks, and condition variables
- Queue-based scheduling system for managing takeoff order
- State machine for aircraft lifecycle (registration, taxiing, clearance, takeoff)

## Technologies

- C
- POSIX Threads (pthreads)
- Sockets (TCP networking)

## Key Concepts Demonstrated

- Concurrency and synchronization (mutexes, rwlocks, condition variables)
- Network programming with sockets
- Thread-safe data structures
- Producer-consumer queue pattern
- Command parsing and protocol design

## Overview

Each airplane connects as a client to the server. The server processes commands such as registration, taxi requests, and takeoff coordination. A dedicated queue manager thread ensures safe takeoff sequencing with proper synchronization between threads.
