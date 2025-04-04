# JSON Verifier and Validator

## Description
Create a JSON validation engine that checks both syntax and schema compliance.

## Problem Statement
Develop a program that validates JSON documents for syntax correctness and schema compliance without using existing JSON libraries.

### Requirements
- Syntax validation
- Schema validation
- Detailed error reporting
- Support for nested structures
- Custom validation rules

### Constraints
1. No JSON parsing libraries
2. Handle large files efficiently
3. Clear error messages
4. Support all JSON data types

## Input Example
```json

{
  "json": "{\"name\": \"test\", \"values\": [1,2,3]}",
  "schema": {
    "type": "object",
    "properties": {
      "name": {"type": "string"},
      "values": {"type": "array", "items": {"type": "number"}}
    }
  }
}
```

## Output Example
```json

{
  "valid": true,
  "errors": [],
  "validation_time_ms": 0.23
}
```


## Success Criteria
- Syntax and Schema Validation is Correct
- Support for Nested Structures
- High level / Detailed Error Reporting
- Parse 1MB JSON under 100ms
- Validate against complex schemas under 250ms
- No use of artificial intelligence or machine learning algorithms should be involved in the creation of your program
