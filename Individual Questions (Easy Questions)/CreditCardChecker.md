# Credit Card Number Validator

## Description
Create a program that validates credit card numbers using the Luhn algorithm.

## Problem Statement
Implement a system that can validate credit card numbers and identify the card issuer.

### Requirements
- Luhn algorithm implementation
- Card issuer identification
- Input format validation
- Error handling
- Support multiple card types

### Constraints
1. No external validation libraries
2. Process single numbers or batches
3. Handle invalid input gracefully
4. Secure number handling

## Input Format
```json
{
  "card_number": "4532015112830366",
  "validate_issuer": true,
  "check_expiry": true,
  "additional_details": {
    "expiry": "05/25",
    "cvv": "123"
  }
}
```

## Output Format
```json
{
  "valid": true,
  "issuer": "VISA",
  "validation_details": {
    "luhn_valid": true,
    "length_valid": true,
    "issuer_valid": true
  },
  "error_code": null
}
```

## Success Criteria
- Validation under 10ms per card
- Batch processing: 1000 cards under 1 second
- 99.99% accuracy rate
- No use of artificial intelligence or machine learning algorithms should be involved in the creation of your program