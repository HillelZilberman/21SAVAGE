# 21SAVAGE

A networked multiplayer card game built in Python using low-level socket programming, TCP/UDP communication, and multithreading.

The project implements a client-server architecture in which clients automatically discover available servers over UDP, establish TCP connections, and play independent game sessions concurrently.

## Key Features

* Client-server architecture using Python sockets
* UDP broadcast-based server discovery
* TCP communication for reliable game sessions
* Multithreaded server with concurrent client handling
* Custom network protocol for structured client/server messages
* Modular separation between networking, session management, and game logic
* Automated tests for networking and protocol components

## Architecture

```text
Client
  │
  │ UDP broadcast discovery
  ▼
Server
  │
  │ TCP connection
  ▼
Client Session  <---->  Server Session
                         │
                         ▼
                     Game Engine
```

The server continuously broadcasts availability over UDP. Clients listen for these offers and use the advertised TCP port to establish a connection.

Each connected client is handled in a separate thread, allowing multiple game sessions to run concurrently.

## Project Structure

```text
21SAVAGE/
├── common/             # Shared network protocol definitions
├── game_engine/        # Core game logic
├── network/
│   ├── client/         # Client networking and entry point
│   └── server/         # Server networking and entry point
├── session/            # Client/server game-session management
├── tests/              # Unit tests for protocol and networking
├── RunGame.py          # Local game runner
└── .gitignore
```

## Running the Networked Game

Clone the repository:

```bash
git clone https://github.com/HillelZilberman/21SAVAGE.git
cd 21SAVAGE
```

### 1. Start the server

From the project root:

```bash
python -m network.server.server_main
```

The server starts listening for TCP connections and broadcasts its availability over UDP.

### 2. Start a client

Open another terminal from the same project directory:

```bash
python -m network.client.client_main
```

The client listens for server offers, connects automatically, and prompts the player for the number of rounds to play.

Additional clients can be started in separate terminals to demonstrate concurrent client handling.

## Running the Local Game

The core game can also be executed without networking:

```bash
python RunGame.py
```

## Tests

The project includes unit tests for the custom protocol and networking components.

Run all tests from the project root:

```bash
python -m unittest discover tests
```

## Technologies & Concepts

* Python
* TCP/IP
* UDP
* Socket Programming
* Multithreading & Concurrency
* Client-Server Architecture
* Network Protocol Design
* Object-Oriented Programming
* Unit Testing

## Authors

Developed as a two-person academic networking project.
