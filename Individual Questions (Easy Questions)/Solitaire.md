# Solitaire Game Engine

## Description
Create a program that implements the classic Solitaire card game with move validation and solution checking.

## Problem Statement
Develop a Solitaire engine that can validate moves, track game state, and determine if a game is winnable.

### Requirements
- Game state management
- Move validation
- Undo/redo functionality
- Win condition detection
- Auto-complete detection

### Constraints
1. Standard Klondike Solitaire rules
2. No external game engines
3. Memory efficient state tracking
4. Must handle all edge cases

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
    ["K♥", "Q♣"],
    // ... more tableaus
  ],
  "waste": ["5♥", "3♣"],
  "stock": ["??", "??", "??"]
}
```

## Move Validation Examples
```
Valid Move 1:
  Source: Q♥ from Tableau
  Destination: K♠ tableau
  Result: VALID

Invalid Move 2:
  Source: 5♥ from Waste
  Destination: 7♣ tableau
  Result: INVALID (wrong color sequence)
```

## Test Scenarios
1. Basic Moves:
   ```
   Move: King to empty tableau
   Expected: Valid move, state updated
   ```

2. Complex Scenarios:
   ```
   Move: Stack of alternating cards
   Expected: Valid if destination card supports it
   ```

3. Auto-complete Detection:
   ```
   State: All cards visible and sorted
   Expected: Detect auto-complete possibility
   ```
