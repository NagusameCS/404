# Scheduling Optimizer

## Description
Create a scheduling system that optimizes resource allocation and time management.

## Problem Statement
Develop an algorithm to optimize scheduling for multiple resources with various constraints and priorities.

### Requirements
- Resource allocation optimization
- Time slot management
- Conflict resolution
- Priority handling
- Schedule validation

### Constraints
1. Handle overlapping schedules
2. Optimize for efficiency
3. Support multiple resource types
4. Real-time updates not required

## Input Format
```json
{
  "resources": [
    {
      "id": "R1",
      "type": "room",
      "availability": ["09:00-17:00"],
      "capacity": 30
    }
  ],
  "events": [
    {
      "id": "E1",
      "duration": 60,
      "required_resources": ["room"],
      "priority": 1,
      "attendees": 25
    }
  ],
  "constraints": {
    "max_concurrent_events": 3,
    "buffer_time": 15
  }
}
```

## Output Format
```json
{
  "schedule": [
    {
      "event_id": "E1",
      "resource_id": "R1",
      "start_time": "09:00",
      "end_time": "10:00"
    }
  ],
  "metrics": {
    "resource_utilization": 0.85,
    "conflicts_resolved": 2
  }
}
```

## Test Cases
1. Basic Scheduling:
   ```
   Input: 3 events, 2 rooms, no conflicts
   Expected: Optimal allocation with max utilization
   ```

2. Conflict Resolution:
   ```
   Input: 2 high-priority events, same time slot
   Expected: Higher priority event gets preferred resource
   ```

3. Complex Constraints:
   ```
   Input: Multiple resource types, varying capacities
   Expected: Valid schedule respecting all constraints
   ```
