# Physics Simulator

## Description
Create a 2D physics engine that simulates basic physical interactions between objects.

## Problem Statement
Develop a physics simulation system that handles collision detection, gravity, and object interactions.

### Requirements
- Collision detection
- Gravity simulation
- Momentum calculations
- Force applications
- Object mass and velocity tracking

### Constraints
1. No physics engine libraries
2. Real-time calculation capability
3. Configurable physics parameters
4. Handle multiple object types

## World Configuration
```json
{
  "world": {
    "gravity": 9.81,
    "air_resistance": 0.01,
    "bounds": {"width": 1000, "height": 1000}
  },
  "objects": [
    {
      "id": "ball1",
      "type": "circle",
      "mass": 1.0,
      "position": {"x": 0, "y": 0},
      "velocity": {"x": 5, "y": 0},
      "radius": 10
    }
  ]
}
```

## Output Format
```json
{
  "frame": 1,
  "time": 0.016,
  "objects": [
    {
      "id": "ball1",
      "position": {"x": 0.08, "y": 0.0016},
      "velocity": {"x": 4.99, "y": -0.157},
      "forces": {"gravity": -9.81, "collision": 0}
    }
  ]
}
```

## Test Scenarios
1. Basic Projectile:
   ```
   Input: Ball thrown at 45 degrees
   Expected: Parabolic trajectory
   ```

2. Collision Detection:
   ```
   Input: Two objects on collision course
   Expected: Elastic collision with momentum conservation
   ```

3. Complex Interactions:
   ```
   Input: Multiple objects with varying masses
   Expected: Accurate force calculations and responses
   ```
