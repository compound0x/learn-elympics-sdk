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

- Elympics Account: Sign up at Elympics Panel

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

### Scene Setup

- Open Assets/Scenes/MainScene.unity

- Ensure the scene has:

  - A Canvas with three buttons (Rock, Paper, Scissors)

  - Two TextMeshProUGUI elements for result and status display

  - GameObjects for GameManager, PlayerData, and Elympics with attached scripts
 
### Scripts

- The project includes the following scripts in Assets/Scripts:

  - GameManager.cs: Manages game logic, UI updates, and server-side winner determination

  - PlayerData.cs: Stores and syncs player moves using Elympics variables

  - ElympicsConfig.cs: Initializes Elympics client

  - MatchmakingManager.cs: Handles matchmaking via Elympics Lobby

  - Web3Integration.cs: Logs match results on-chain

### Build and Deploy

- Build the Game:

  - In Unity, go to Elympics > Build Game

  - Select “Client and Server” and build for WebGL platform

- Deploy to Elympics Cloud:

  - In the terminal, navigate to the project folder and run:
    ```
    elympics build-upload
    ```
  - Upload the build and assign it to your Game Version in the Elympics Panel
 
- Test Locally:

  - Use Elympics > Run Local Server to test with two Unity instances
 
## Gameplay

- Players join a match via Elympics matchmaking

- Each player selects a move (Rock, Paper, or Scissors)

- The server compares moves and determines the winner (Rock > Scissors, Paper > Rock, Scissors > Paper)

- Results are displayed on-screen and optionally logged on-chain

## Web3 Integration

- Enable Web3 in the Elympics Panel

- Use Web3Integration.cs to log match results to the blockchain

- Configure rewards in the Elympics Panel (requires wallet setup)

## Folder Structure

```
learn-elympics-sdk/
├── Assets/
│   ├── Scenes/
│   │   └── MainScene.unity
│   ├── Scripts/
│   │   ├── GameManager.cs
│   │   ├── PlayerData.cs
│   │   ├── ElympicsConfig.cs
│   │   ├── MatchmakingManager.cs
│   │   └── Web3Integration.cs
│   └── Elympics/ (SDK files)
└── README.md
```

## Troubleshooting

- Matchmaking Issues: Check Game ID/Secret Key in ElympicsBehaviour

- Sync Errors: Ensure PlayerData is assigned to ElympicsBehaviour

- CLI Errors: Verify Node.js and Elympics CLI installation

- Logs: Use Unity Console and Elympics Panel for debugging

## Resources

- Elympics Documentation https://docs.elympics.ai

- Elympics GitHub https://github.com/Elympics

- Elympics Panel https://console.elympics.ai

## Contributing

Feel free to fork this repository, submit issues, or create pull requests to improve the game!

## License

MIT License (see LICENSE file)
