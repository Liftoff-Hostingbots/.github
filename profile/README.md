# Liftoff Hostingbots

> Automated lobby hosting infrastructure for the drone racing game **Liftoff**.

---

## Overview

**Liftoff Hostingbots** is an open-source infrastructure project designed to automate lobby creation and management for the FPV drone racing game [Liftoff](https://store.steampowered.com/app/410340/Liftoff_FPV_Drone_Racing/). The system uses a combination of a game interaction bot, a Java backend, and a React frontend to providing a looby hosting bot when no one wants to be host.

---

## Repositories

| Repository | Description | Language |
|---|---|---|
| [Liftoff-Lobby-Bot](https://github.com/Liftoff-Hostingbots/Liftoff-Lobby-Bot) | Main lobby bot and game interacter — uses autoclicker and screen positioning to interact with the game | Java |
| [Java-Backend](https://github.com/Liftoff-Hostingbots/Java-Backend) | REST backend for interacting with the PostgreSQL database, serving the frontend application | Java |
| [Frontend](https://github.com/Liftoff-Hostingbots/Frontend) | Web application for users to view and interact with hosted lobbies | TypeScript (React) |

---

## Architecture

```
┌──────────────────┐       ┌──────────────────┐       ┌──────────────────┐   ┌──────────────────┐
│                  │       │                  │       │                  │   |                  |
│  Liftoff Game    │◄─────►│  Lobby Bot       │──────►│  Java Backend    │   |  PostgreSQL DB   |
│  (Desktop App)   │       │  (Autoclicker)   │       │    (REST API)    │──►|                  |
│                  │       │                  │       │        │         │   |                  |
└──────────────────┘       └──────────────────┘       │  PostgreSQL DB   │   |                  |  
                                                      └────────┼─────────┘   └────────┼─────────┘
                                                               │
                                                      ┌────────▼─────────┐
                                                      │                  │
                                                      │  React Frontend  │
                                                      │  (TypeScript)    │
                                                      │                  │
                                                      └──────────────────┘
```

---

## Getting Started

Each component lives in its own repository. Follow the setup instructions in each repo's README:

1. **Backend** — Set up the Java backend and connect it to your PostgreSQL database.
2. **Lobby Bot** — Configure and run the lobby bot on a machine with Liftoff installed.
3. **Frontend** — Start the React frontend to monitor and manage hosted lobbies.

---

## Tech Stack

- **Bot:** Autoclicker / screen positioning automation
- **Backend:** Java + PostgreSQL
- **Frontend:** React + TypeScript

---

## Contributing

Contributions, issues, and feature requests are welcome! Feel free to open an issue or pull request in the relevant repository.

---

## Contact

**Email:** [magnus.thor@live.dk](mailto:magnus.thor@live.dk)

---

*Made with ❤️ for the Liftoff FPV community.*
