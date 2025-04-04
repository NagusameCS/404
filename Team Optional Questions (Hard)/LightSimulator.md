# Light Ray Simulator

## Description
Create a program that simulates light ray behavior including reflection and refraction.

## Problem Statement
Implement a system that accurately models light behavior through different mediums and surfaces.

### Requirements
- Reflection calculations
- Refraction modeling
- Surface interaction
- Ray tracing
- Multiple light sources

### Constraints
1. No graphics libraries
2. Physical accuracy required
3. Support multiple surface types
4. Handle complex geometries

## Input Format
```json
{
  "scene": {
    "dimensions": {"width": 1000, "height": 1000},
    "light_sources": [{
      "position": {"x": 0, "y": 0},
      "intensity": 1.0,
      "wavelength": 550
    }],
    "objects": [{
      "type": "mirror",
      "position": {"x": 100, "y": 100},
      "angle": 45,
      "refractive_index": 1.5
    }]
  }
}
```

## Output Format
```json
{
  "rays": [{
    "path": [
      {"x": 0, "y": 0},
      {"x": 100, "y": 100},
      {"x": 200, "y": 0}
    ],
    "intensity": 0.85,
    "interactions": [{
      "type": "reflection",
      "position": {"x": 100, "y": 100},
      "angle_of_incidence": 45
    }]
  }]
}
```

## Test Cases
1. Simple Reflection:
   ```
   Input: Single mirror, single ray
   Expected: Perfect reflection angle
   ```

2. Multiple Media:
   ```
   Input: Ray passing through water to glass
   Expected: Correct refraction angles
   ```
