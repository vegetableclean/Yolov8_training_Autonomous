# Dataset Collection Guidelines for YOLO-seg Fine-Tuning

## 1. QCar
- **Number of Images**: 500 - 1000
- **Image Types / Scenarios**:
  - Front view of the car
  - Side view (left and right)
  - Rear view
  - Different distances: close, medium, far
  - Different lighting conditions: daytime, nighttime, shadows
  - Various backgrounds: urban streets, parking lots, highways
  - Partial occlusion (e.g., other cars, pedestrians)
  - Different weather conditions: sunny, cloudy, rainy (if possible)

## 2. Road Signs
- **Number of Images**: 300 - 600
- **Image Types / Scenarios**:
  - Front-facing signs (clear view)
  - Angled view (slightly rotated, perspective)
  - Different distances
  - Different lighting: bright daylight, dusk, night
  - Signs partially occluded by trees, poles, or other objects
  - Different environments: urban, suburban, highways

## 3. Traffic Lights
- **Number of Images**: 400 - 800
- **Image Types / Scenarios**:
  - Front view (green, yellow, red)
  - Side/angled view
  - Different distances
  - Daytime and nighttime
  - Occluded or partially blocked lights
  - Different traffic light types: hanging, pole-mounted
  - Various backgrounds: intersections, highways, urban streets

## Additional Notes
- Each image should ideally contain **at least one object of interest**.
- Bounding boxes do not need to be perfect; they should **fully cover the object**.
- Use diverse environments and conditions to improve model robustness.
- Optionally, use **Segment Anything Model (SAM)** to generate initial masks for segmentation tasks.
