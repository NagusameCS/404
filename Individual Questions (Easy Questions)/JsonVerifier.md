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

## Input/Output Examples
```json
// Input Example
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

// Output Example
{
  "valid": true,
  "errors": [],
  "validation_time_ms": 0.23
}
```

## Test Cases
1. Syntax Validation:
   ```json
   Input: "{\"key\": value}"
   Expected: {"valid": false, "errors": ["Missing quotes around string value"]}
   ```

2. Schema Validation:
   ```json
   Input: {"age": "25"}
   Schema: {"age": {"type": "number"}}
   Expected: {"valid": false, "errors": ["Type mismatch: expected number"]}
   ```

## Performance Requirements
- Parse 1MB JSON under 100ms
- Validate against complex schemas under 250ms
- Memory usage under 50MB for 10MB files
- No use of artificial intelligence or machine learning algorithms should be involved in the creation of your program