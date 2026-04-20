# Game Lights Out

## Project Description
Game Lights Out is a 5x5 interactive puzzle game built using React. The objective of the game is to turn all the lights OFF. When a player clicks on a light, it toggles itself and its adjacent (up, down, left, right) lights.

The game includes multiple difficulty levels and ensures that every generated puzzle is always solvable.

## Features
- 5x5 interactive grid (25 lights)
- Click toggles light + adjacent neighbors
- Always solvable puzzle generation
- Difficulty levels:
  - Easy
  - Medium
  - Hard
- Move counter
- Undo feature
- Reset / New Game option
- Win detection ("You Win!" message)

## Technologies Used
- React (Vite)
- JavaScript (ES6)
- CSS (for styling only)

## Project Structure

- Game.jsx → Main logic (state, levels, win condition)
- Grid.jsx → Renders 5x5 grid
- Light.jsx → Single light component
- index.css → UI styling

## How Game Works

1. Game starts with a solvable random board.
2. Player clicks a light.
3. The clicked light and its neighbors toggle ON/OFF.
4. Player tries to turn all lights OFF.
5. Game shows "You Win!" when all lights are OFF.

## Key React Concepts Used

### 1. Components
- Game
- Grid
- Light

### 2. State Management (useState)
- Board state (lights)
- Move history
- Current step
- Difficulty level

### 3. Props
- Grid passes data to Light component
- Click handlers passed from parent to child

### 4. Lifting State Up
- Game component manages full state (board + history)
- Grid and Light are only presentational

## Undo Feature
The game stores all previous states in a history array. Undo allows the player to go back to a previous state.

## Solvability Logic
Instead of random true/false values, the board is created by:
- Starting from an empty board
- Applying random valid flips

This guarantees every puzzle is solvable.

## How to Run
npm install
npm run dev