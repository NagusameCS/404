# Enigma Machine Simulator

## Description
Create a simulator for the WWII Enigma encryption machine.

## Problem Statement
Implement a working model of the Enigma machine including rotor mechanics and encryption/decryption capabilities.

### Requirements
- Rotor implementation
- Plugboard configuration
- Encryption/decryption
- Historical accuracy
- State tracking

### Constraints
1. Match historical specifications
2. No cryptographic libraries
3. Support all historical rotors
4. Include reflector mechanics

## Configuration Format
```json
{
  "rotors": [
    {"type": "I", "position": "A", "ring_setting": 1},
    {"type": "II", "position": "B", "ring_setting": 2},
    {"type": "III", "position": "C", "ring_setting": 3}
  ],
  "reflector": "B",
  "plugboard": ["AB", "CD", "EF"]
}
```

## Input/Output Examples
```
Input Message: "ATTACKATDAWN"
Rotor Settings: I-II-III, Positions: AAA
Plugboard: AB CD EF
Output: "UFQFXECTDQNT"

Input Message: "UFQFXECTDQNT"
Same Settings
Output: "ATTACKATDAWN"
```

## Success Criteria
- The simulator must correctly implement the behavior of the Enigma rotors, including their ability to rotate after each keypress.
- Support for all historical rotors (e.g., I, II, III, IV, V).
- Each rotor should correctly map input letters to output letters based on the rotor’s wiring.
- The simulator must correctly implement plugboard functionality, allowing swaps between specific pairs of letters.
- Plugboard configuration should follow the provided input format (e.g., ["AB", "CD", "EF"]), where letters are swapped before entering and after leaving the rotors.
- The reflector should be implemented according to historical specifications, with the input letter being reflected back through the rotors, without altering the plugboard.
- The machine must be able to encrypt and decrypt messages using the same configuration (rotors, positions, plugboard, and reflector).
- The same input message should return to the original message after being encrypted and then decrypted using identical settings.
- No use of artificial intelligence or machine learning algorithms should be involved in the creation of your program
