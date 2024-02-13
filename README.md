# Reaction Timer Game

## Screenshots

![](https://raw.githubusercontent.com/elvan/reaction-timer-game-vue-example/main/__screenshots__/Screenshot%202024-02-13%20202010.png)

---

![](https://raw.githubusercontent.com/elvan/reaction-timer-game-vue-example/main/__screenshots__/Screenshot%202024-02-13%20202052.png)

## Description

The Reaction Timer Game is a Vue.js project designed to test and improve users' reaction times in a fun and interactive way. It challenges players to respond to visual cues with speed and accuracy, offering a dynamic way to gauge and enhance reflexes over time.

## Features

- **Project Setup and Initial Files** - The foundation of the project was established with essential configurations for browser compatibility, consistent coding styles, and a basic Vue app structure, including a .browserslistrc, .editorconfig, and initial Vue component setup.

- **Gameplay and Block Component** - Introduced gameplay logic and the Block component, enabling interactive game elements and conditional rendering based on game state. Gameplay begins with a random delay, and the UI was enhanced for a better player experience.

- **End Game Functionality and Block Improvements** - Added functionality to dynamically show the Block based on a timer and implemented an "End game" button, allowing players to stop the game as needed.

- **Refinement of Game Logic** - Simplified the game by removing the "End game" button and enhancing the Block component with reaction timer logic, including start and stop timer methods for an interactive gameplay experience.

- **Score Display and End Game Logic** - Implemented a score display system that shows reaction time results after the game ends, providing immediate feedback on player performance.

- **Results Component for Displaying Scores** - Introduced a Results component to manage score display more efficiently, organizing the code structure for clearer component interaction.

- **Ranking System in Results Component** - Enhanced the Results component with a dynamic ranking system based on the player's score, offering ranks like Ninja Fingers, Rapid Reflexes, and Snail Pace, along with styled rank display for visual emphasis.

## Installation

### Prerequisites

- Node.js and npm installed on your system

### Environment Setup

1. Clone the repository to your local machine.
2. Navigate to the project directory.

### Installation Commands

```bash
# Install dependencies
npm install

# Serve with hot reload at localhost:8080
npm run serve

# Build for production with minification
npm run build
```

## Usage

After setting up the project, you can start the game by clicking the "play" button. The game will randomly display a block that you need to click as fast as possible. Your reaction time will be measured and displayed at the end of each round, along with a ranking based on your performance.
