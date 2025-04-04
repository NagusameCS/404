# Poker Bots Challenge

## Description
Create an AI bot that can play poker against other bots in a tournament setting.

## Problem Statement
Develop a poker-playing bot that implements strategic decision-making for Texas Hold'em poker.

### Requirements
- Bot must make decisions based on:
  - Current hand
  - Pot odds
  - Position
  - Opponent behavior patterns
- Must implement betting, calling, folding logic
- Tournament-ready format for bot vs bot matches
- No use of artificial intelligence or machine learning algorithms should be involved in the creation of your program

### Constraints
1. No external AI libraries
2. Fixed time limit for decisions
3. Standard poker rules apply
4. Must handle all poker scenarios

## Game Specifications
- Texas Hold'em No-Limit
- 6-player table maximum
- 1000 starting chips per player
- Small blind: 10, Big blind: 20

## Bot Requirements
1. Decision Making
   - Pre-flop action
   - Post-flop action
   - River and Turn decisions
   - All-in considerations
   
2. Strategy Implementation
   - Position-based play
   - Stack size awareness
   - Opponent modeling
   - Bluff detection

## Example Scenarios

### Scenario 1: Basic Decision
```
Hand: [A♠, K♠]
Position: Button
Action: 2 folds, 1 raise to 60
Bot should: Call (due to strong hand, position)
```

### Scenario 2: Complex Decision
```
Hand: [J♥, J♣]
Board: [J♠, 7♥, 2♣]
Pot: 240
Opponent bet: 120
Stack sizes: Bot(800), Opponent(600)
Bot should: Raise to 360 (set value betting)
```

## Performance Metrics
1. Win rate in bot-vs-bot matches
2. Chip accumulation efficiency
3. Decision speed (<1 second/action)
4. Bluff success rate
5. Hand reading accuracy

## Tournament Format
- 6 bots per table
- 10,000 hands minimum
- Double elimination structure
- Increasing blind levels
