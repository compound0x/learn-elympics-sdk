# learn-elympics-sdk

A simple two-player Rock, Paper, Scissors multiplayer game built in Unity with the Elympics SDK for server-authoritative gameplay and Web3 integration. Players select a move (Rock, Paper, or Scissors), and the server determines the winner, ensuring fair and synchronized results. The game supports matchmaking and can log results on-chain for leaderboards or rewards.

## Features

- Multiplayer: Two players compete in real-time via Elympics' server-authoritative architecture

- Elympics Integration: Handles matchmaking, synchronization, and server-side logic

- UI: Simple Unity UI with buttons for Rock, Paper, Scissors and text displays for results

- Web3: Logs match results on-chain using Elympics API

- Scalable: Deployable to Elympics Cloud for cross-platform play

## Prerequisites

- Unity: 2021.3 LTS or later

- Elympics SDK: Install via Unity Package Manager

- Node.js: For Elympics CLI

- Elympics Account: Sign up at Elympics Developer Console

- Git: For repository management

## Setup Instructions

### Clone the Repository

```
git clone https://github.com/compound0x/learn-elympics-sdk.git
cd learn-elympics-sdk
```

### Setup Unity Project

- Open Unity Hub and add the project folder (learn-elympics-sdk)

- Use Unity 2021.3 LTS or later

- Open the MainScene in Assets/Scenes

### Install Elympics SDK

- In Unity, go to Window > Package Manager

- Click the “+” icon, select “Add package from git URL”, and enter:
  ```
  https://github.com/Elympics/Unity-SDK.git
  ```
  
- Verify the “Elympics” menu appears in Unity’s toolbar

### Configure Elympics

- Sign up at Elympics Panel and create a new game profile

- Note the Game ID and Secret Key

- In Unity, create a GameObject named “Elympics” and add the ElympicsBehaviour component

- Assign the Game ID and Secret Key in the ElympicsBehaviour Inspector

### Install Elympics CLI

- Install Node.js

- Open a terminal and install the Elympics CLI:
  ```
  npm install -g @elympics/cli
  ```
  
- Log in
  ```
  elympics login
  ```
