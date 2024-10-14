# Catch The Thief - Demo

**Catch The Thief** is a turn-based puzzle game built in Unity where players control police officers on a connected node graph. The goal is to strategically position the officers to block the thief's movements using strategic gameplay.

This repository contains only the web demo build of the project. The source code is not included here to protect the integrity of the project for future development and release.

## Demo

You can play the demo on Vercel using the following link: [Catch The Thief - Demo](https://catch-the-thief-demo.vercel.app)

## How to Play

- **Objective:** Block all possible moves of the thief by positioning police officers on the connected node graph.
- **Turn-based Gameplay:** Each turn, the player moves one police officer. After each move, the thief automatically moves to an adjacent, unoccupied node.
- **Thief's Movement:** The thief moves randomly to a connected node after the player's turn.
- **Current State:** There is currently no implemented win condition; the game continues with the thief making random available movements. Future updates will include the win state logic.

## Technologies and Concepts Used

This section details the core technologies and concepts used to develop the game:

### 1. **Unity Engine (2023.x)**
   - **2D Game Development**: Built using Unity’s 2D framework, including the use of its physics engine for grid-based movement.
   - **Scene Management**: The game uses Unity’s scene and object management system to handle levels, nodes, and game characters.

### 2. **C# Programming**
   - **Game Logic**: All game logic, including player input handling, AI movement, and turn-based mechanisms, are implemented in C#.
   - **Drag-and-Drop System**: Implemented using Unity's event system (`OnPointerDown`, `OnDrag`, `OnPointerUp`).

### 3. **Visual Effects with Shader Graph**
   - **Custom Visual Effects**: For visual feedback during the drag-and-drop interactions, I implemented a **custom outline effect** using **Unity’s Sprite Unlit Shader Graph**. This effect highlights the selected police officer with a glowing outline, enhancing the player's experience during movement.
   - **Shader Graph Usage**: Shader Graph is used here to visually indicate when an officer is being dragged, which dynamically changes based on user interaction.
   
### 4. **Graph Theory for Node-Based Movement**
   - The game world is structured as a **graph**, where:
     - **Nodes** represent possible positions for characters.
     - **Edges** represent the valid connections between nodes.
   - The police officers and thief move between these nodes, following the graph connections.
   - This approach allows for strategic positioning and constraint-based movement.

### 5. **Randomized AI Movement**
   - The thief's movement is based on a **randomized algorithm**:
     - The thief selects a random adjacent node that is unoccupied.
     - Future updates could involve pathfinding algorithms (e.g., **A* or Dijkstra's algorithm**) to make the AI more intelligent.

### 6. **WebGL Deployment (Vercel)**
   - The game is built as a **WebGL project** and deployed on Vercel for easy access and sharing.
   - This allows the game to run directly in the browser, showcasing the demo without any installation required.

### 7. **Optimization for Performance**
   - Performance optimizations include object pooling and careful management of memory to ensure smooth gameplay in a web environment.

## Future Improvements

- **Win Condition Logic**: Implementing game-over detection when the thief is fully blocked by police.
- **AI Enhancements**: Introduce smarter movement for the thief based on pathfinding algorithms, making the game more challenging.
- **Graph Expansion**: Add varying graph layouts and introduce complexity in node types, e.g., locked nodes, one-way paths.
- **UI Enhancements**: Improve the user interface with better indicators for valid/invalid moves.

## License

The demo is for viewing purposes only. The full source code and project are proprietary and will be used for future releases, including a potential launch on mobile platforms.
