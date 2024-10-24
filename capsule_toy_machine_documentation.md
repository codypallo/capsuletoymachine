
# Capsule Toy Machine Developer Documentation

## Overview

The Capsule Toy Machine is an open-source console designed to host and serve **WebXR content** packaged as **ePub files**. This platform is built for long-term, offline-first use, and ensures that WebXR experiences can be shared and experienced without reliance on centralized services or cloud infrastructure.

---

## Getting Started

### Prerequisites

To start developing for the Capsule Toy Machine, ensure you have the following:

- **Node.js**: Install Node.js for local development.
- **A-Frame**: The framework for building WebXR experiences, available at [A-Frame.io](https://aframe.io).
- **Docker**: Used to create containerized apps for deployment on platforms like Zimaboard or Casa OS.

---

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/codypallo/capsuletoymachine.git
    ```

2. Navigate to the project directory:
    ```bash
    cd capsuletoymachine
    ```

3. Install dependencies:
    ```bash
    npm install
    ```

4. Optional: Start Docker for containerized deployment:
    ```bash
    docker-compose up
    ```

---

## Running the Development Server

To run your WebXR project locally for development:
```bash
npm run start
```
This will serve your WebXR app on your local machine.

---

## Packaging for Capsule Toy Machine

Once your app is ready, you can package it as an ePub file:
```bash
npm run build-epub
```
This will create a distributable ePub file of your project.

---

## API Documentation

- **Multiplayer API**: Real-time multiplayer experiences using [Networked-Aframe](https://github.com/networked-aframe/networked-aframe).
- **Peer-to-Peer Content Sharing API**: Built with [WebTorrent](https://github.com/webtorrent/webtorrent).
- **Voice & Video Chat API**: Using [SimplePeer](https://github.com/Hishammpsnhn/react-socket-simplePeer).
- **Custom Input API**: Support for custom controllers using [WebXR Input Profiles](https://github.com/immersive-web/webxr-input-profiles).
- **Offline Analytics**: Local user tracking with [Matomo](https://github.com/matomo-org/matomo).
- **More APIs**: Full documentation is available in the `/docs` folder of this repository.

---

## Roadmap

### Phase 1: Core Features & Infrastructure
- **A-Frame Boilerplate**: Set up the foundation for A-Frame WebXR development.
- **ePub Packaging**: Provide a mechanism for packaging A-Frame projects into ePub format.
- **Local Server Instance**: Automatically spin up a local server instance to serve content.

### Phase 2: API Development
- **Multiplayer API**: Implement `Networked-Aframe` for real-time multiplayer experiences.
- **Peer-to-Peer Content Sharing API**: Use `WebTorrent` for offline content sharing.
- **Voice and Video Chat API**: Integrate `SimplePeer` for offline voice and video chat.
- **Custom Input API**: Support custom controllers via `WebXR Input Profiles`.
- **Offline Analytics API**: Implement `Matomo` for local user tracking.

---

## Contributing

We encourage contributions from the community. Please feel free to open issues, submit pull requests, or fork the repository to develop your own projects. Together, we can build a decentralized future for immersive content.

---

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
