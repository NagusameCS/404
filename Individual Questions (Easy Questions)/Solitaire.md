# Solitaire Game Engine

## Problem Statement
Design and implement a game engine for Klondike Solitaire that accurately simulates gameplay, validates player moves, tracks game state efficiently, supports undo/redo functionality, and detects win conditions and auto-completion scenarios.

## Description
The goal is to create a backend engine for the classic Klondike Solitaire game. This engine must encapsulate all game logic without the use of external game engines. It must be able to validate each move according to official rules, provide robust state management, and support automated tests to verify correctness.

## Requirements
- **Game State Management**: Track all cards across foundations, tableaus, waste, and stock.
- **Move Validation**: Ensure only legal moves are executed (e.g., alternating colors, correct sequences).
- **Undo/Redo**: Allow the user to revert and reapply moves without loss of state.
- **Win Detection**: Detect when all cards have been correctly moved to foundations.
- **Auto-complete Detection**: Identify when the game is effectively won and can auto-complete.

## Constraints
1. Must follow standard Klondike Solitaire rules strictly.
2. No use of external or third-party game engines.
3. State tracking must be memory efficient and scalable.
4. All edge cases (e.g., empty tableau moves, draw pile exhaustion) must be handled gracefully.

## Game State Format
```json
{
  "foundations": {
    "hearts": ["A", "2", "3"],
    "diamonds": ["A"],
    "clubs": [],
    "spades": ["A", "2"]
  },
  "tableaus": [
    ["K♠", "Q♥", "J♠"],
    ["K♥", "Q♣"]
  ],
  "waste": ["5♥", "3♣"],
  "stock": ["??", "??", "??"]
}
```

## Move Validation Examples
```
Valid Move 1:
  Source: Q♥ from Tableau
  Destination: K♠ in Tableau
  Result: VALID

Invalid Move 2:
  Source: 5♥ from Waste
  Destination: 7♣ in Tableau
  Result: INVALID (wrong color sequence)
```

## Test Scenarios
### 1. Basic Moves
```
Move: King to empty tableau
Expected: Valid move, state updated
```

### 2. Complex Stack Moves
```
Move: Stack of alternating cards from one tableau to another
Expected: Valid only if bottom card matches destination rule
```

### 3. Auto-complete Detection
```
State: All cards visible and sorted appropriately
Expected: Auto-complete condition recognized
```

### 4. Undo/Redo
```
Action: Perform move, undo, redo
Expected: State transitions match previous and next correctly
```

### 5. Win Detection
```
Condition: All foundations complete (A to K in each suit)
Expected: Win condition triggered
```

### 6. Edge Case: Empty Stock
```
Condition: Stock exhausted, cards recycled from waste
Expected: Stock refilled correctly, play continues
```

