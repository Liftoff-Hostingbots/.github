# Liftoff Lobby Hosting Bots System

A system that allows users to interact with live lobbies in Liftoff through automated bots, participate in lobby voting, and submit actions via a web interface.

---

# Architecture Overview

This project is structured as a **multi-repository system** where each component has a single responsibility.

```
Frontend  ---> Backend API
Liftoff Bot ---> Backend API
Backend   ---> Database
```

The backend acts as the **single source of truth** for all game state, voting, and submissions.

---

# Repositories

## 1. game-bot

Responsible for interacting directly with the Liftoff game.

### Responsibilities

* Sending commands to Liftoff lobbies
* Listening to lobby/game events
* Executing voted lobby actions
* Communicating with backend
* Communicating with players
---

## 2. backend

### Responsibilities

* Lobby state management
* Voting logic
* Submission handling
* Game session state
* API for bot + frontend
* Users/Profiles
* Authentication

### Owns

* Database
* Game state
* User actions

---

## 3. frontend

User interface for interaction.

### Responsibilities

* Lobby display
* Voting UI
* Community Track submissions

### Communicates with

Backend only.

---

# Deployment Model

Each component is independently deployable.

This allows:

* Updating UI without restarting bot
* Scaling backend separately
* Running bot locally for testing

---

# Development Setup

Each repository contains its own setup instructions.

Typical local flow:

1. Run database
2. Run backend
3. Run bot
4. Run frontend

---

# 🎯 Design Principles

* Single responsibility per repo
* Backend owns all state
* No direct DB access outside backend
* Independent deployment
* Clear API contracts

---

# Future Development

* Multiple bots
* Multiple lobbies
* CICD Pipelines
