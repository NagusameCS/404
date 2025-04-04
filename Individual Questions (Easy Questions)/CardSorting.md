# Card Sorting Algorithm

## Description
Implement a specialized sorting algorithm for playing cards.

## Problem Statement
Create an efficient algorithm to sort a deck of cards by suit and rank.

### Requirements
- Sort by suit (♥, ♦, ♣, ♠)
- Sort by rank (2-10, J, Q, K, A)
- Handle multiple decks
- Track sorting operations

### Constraints
1. No built-in sorting functions
2. O(n log n) time complexity target
3. Memory efficient implementation
4. Handle invalid cards

## Input Format
```json
{
  "cards": [
    {"suit": "♥", "rank": "7"},
    {"suit": "♠", "rank": "A"},
    {"suit": "♥", "rank": "K"}
  ],
  "sort_priority": ["suit", "rank"]
}
```

## Expected Output
```json
{
  "sorted_cards": [
    {"suit": "♥", "rank": "7"},
    {"suit": "♥", "rank": "K"},
    {"suit": "♠", "rank": "A"}
  ],
  "metrics": {
    "comparisons": 3,
    "swaps": 1,
    "time_ms": 0.15
  }
}
```

## Test Cases
1. Standard Deck:
   ```
   Input: Full 52-card deck shuffled
   Expected: Sorted by suit (♠,♥,♣,♦) then rank (2-A)
   ```

2. Multiple Decks:
   ```
   Input: Two decks mixed together
   Expected: Sorted with duplicates maintained
   ```

3. Invalid Cards:
   ```
   Input: {"suit": "Invalid", "rank": "13"}
   Expected: Error report with invalid card identification
   ```


## Success Criteria
- Cards must be sorted first by suit in the order ♠ < ♥ < ♣ < ♦ (or as defined) and then by rank in the order 2–10 < J < Q < K < A.
- Sorting order must follow the sort_priority field in the input (e.g., ["suit", "rank"] or ["rank", "suit"]).
- The algorithm must correctly sort multiple decks, maintaining duplicates.
- Sorting must be implemented without using any built-in sort functions (e.g., sort(), sorted() in Python).
- The implemented algorithm should achieve a target time complexity of O(n log n).
- The algorithm must avoid excessive memory use; prefer in-place sorting or minimal auxiliary space.
- Output must include metrics for the number of comparisons, swaps, and time taken in milliseconds.
- Input containing cards with invalid suits or ranks must trigger appropriate error reporting.
- Final output must follow the specified JSON structure, including sorted_cards and metrics.
- No use of artificial intelligence or machine learning algorithms should be involved in the creation of your program