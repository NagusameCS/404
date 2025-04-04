# Puzzle Solving AI

## Description
Create an AI system capable of solving various types of logic puzzles.

## Problem Statement
Develop an algorithm that can analyze and solve different types of logic puzzles using heuristic approaches.

### Requirements
- Pattern recognition
- Rule-based solving
- Multiple puzzle type support
- Solution validation
- Step-by-step solution tracking

### Constraints
1. No machine learning
2. No external AI libraries
3. Efficient memory usage
4. Support custom puzzle types

## Input Format
```json
{
  "puzzle_type": "sudoku",
  "initial_state": [
    [5,3,0,0,7,0,0,0,0],
    [6,0,0,1,9,5,0,0,0],
    [0,9,8,0,0,0,0,6,0]
    // ... remaining rows
  ],
  "constraints": {
    "valid_numbers": [1,2,3,4,5,6,7,8,9],
    "unique_in_row": true,
    "unique_in_column": true,
    "unique_in_block": true
  }
}
```

## Output Format
```json
{
  "solution": [
    [5,3,4,6,7,8,9,1,2],
    [6,7,2,1,9,5,3,4,8],
    // ... remaining rows
  ],
  "steps": [
    {
      "position": [0,2],
      "value": 4,
      "reasoning": "Only possible number in row"
    }
  ],
  "metrics": {
    "time_ms": 45,
    "steps_taken": 12,
    "backtracking_count": 2
  }
}
```

## Test Cases
1. Simple Puzzle:
   ```
   Input: Nearly complete Sudoku
   Expected: Solution in < 10 steps
   ```

2. Complex Logic:
   ```
   Input: Expert level puzzle
   Expected: Complete solution with reasoning
   ```
