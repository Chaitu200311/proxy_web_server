# Multithreaded Proxy Web Server

## Overview
This is a high-performance multithreaded proxy web server that efficiently handles multiple client requests. It supports caching using an LRU (Least Recently Used) policy to improve response times by serving frequently accessed content from memory. The server is implemented in C, leveraging system calls, threading, and synchronization mechanisms for optimal performance.

## Features
- **Multithreading**: Handles multiple concurrent client requests using POSIX threads.
- **Caching**: Implements an LRU-based cache to store frequently accessed web pages, reducing network latency.
- **Concurrency Control**: Utilizes mutex locks and semaphores for safe access to shared resources.
- **Socket Programming**: Facilitates TCP-based client-server communication.
- **Memory Management**: Efficiently manages memory allocation for caching and request processing.

## Technologies Used
- C (POSIX Threads, Sockets, System Calls)
- TCP/IP Networking
- LRU Cache Implementation
- Mutexes and Semaphores for Synchronization

## Installation & Setup
### Prerequisites
Ensure you have the following installed:
- GCC (for compiling C programs)
- Linux-based environment (Ubuntu, CentOS, etc.)

### Build and Run
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/multithreaded-proxy-server.git
   cd multithreaded-proxy-server
   ```

2. Compile the proxy server:
   ```bash
   gcc -pthread -o proxy_server proxy_server.c
   ```

3. Run the server:
   ```bash
   ./proxy_server <port>
   ```
   Replace `<port>` with the desired port number (e.g., 8080).

4. Configure your web browser or client to use `localhost:<port>` as a proxy server.

## Usage
- The proxy server listens on the specified port and forwards client requests to the destination web server.
- Cached responses are served directly without forwarding requests when available.
- Logs and debug messages can be added for monitoring requests and cache status.

## Future Enhancements
- Support for HTTPS traffic
- Logging and request tracking
- Dynamic cache size adjustment
- Performance optimizations for high-traffic environments

## Contributing
Contributions are welcome! Feel free to submit issues, bug reports, or pull requests.

## License
This project is licensed under the MIT License. See `LICENSE` for details.

---
Feel free to customize the README further based on your implementation details.

