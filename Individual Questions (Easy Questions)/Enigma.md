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

Here are the success criteria for the Enigma Machine Simulator problem:

⸻

## Success Criteria
	1.	Rotor Mechanics Implementation
	•	The simulator must correctly implement the behavior of the Enigma rotors, including their ability to rotate after each keypress.
	•	Support for all historical rotors (e.g., I, II, III, IV, V).
	•	Each rotor should correctly map input letters to output letters based on the rotor’s wiring.
	2.	Plugboard Configuration
	•	The simulator must correctly implement plugboard functionality, allowing swaps between specific pairs of letters.
	•	Plugboard configuration should follow the provided input format (e.g., ["AB", "CD", "EF"]), where letters are swapped before entering and after leaving the rotors.
	3.	Reflector Mechanics
	•	The reflector should be implemented according to historical specifications, with the input letter being reflected back through the rotors, without altering the plugboard.
	4.	Encryption/Decryption Capability
	•	The machine must be able to encrypt and decrypt messages using the same configuration (rotors, positions, plugboard, and reflector).
	•	The same input message should return to the original message after being encrypted and then decrypted using identical settings.
Example:
	•	Encrypt “ATTACKATDAWN” and then decrypt the resulting ciphertext to get back “ATTACKATDAWN”.
	5.	State Tracking
	•	The simulator must track the state of the machine, including rotor positions, ring settings, and plugboard configuration.
	•	The state should be accurately updated after each keypress, with the rotors rotating and the plugboard swapping letters as specified.
	6.	Historical Accuracy
	•	The machine should adhere to the historical specifications of the Enigma machine:
	•	Correct rotor wiring and rotations.
	•	Reflector behavior (e.g., reflector type B, C, etc.).
	•	Use of ring settings that adjust the rotor wiring position.
	7.	No Use of Cryptographic Libraries
	•	The simulation should not rely on any cryptographic libraries or external encryption functions. The implementation must rely solely on simulating the mechanics of the Enigma machine.
	8.	Accurate Input and Output Format
	•	Input and output must match the specified format:
	•	Input message: Alphanumeric uppercase letters.
	•	Output message: Encrypted or decrypted uppercase letters.
	•	Rotor configuration, plugboard settings, and reflector type must be correctly parsed and applied.
- No use of artificial intelligence or machine learning algorithms should be involved in the creation of your program