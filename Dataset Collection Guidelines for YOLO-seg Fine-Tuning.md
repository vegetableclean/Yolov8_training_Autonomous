# Dataset Collection Guidelines for YOLO-seg Fine-Tuning

## 1. Person / Pedestrian
- **Class ID**: 1  # Same as COCO "person"
- **Number of Images**: 400 - 800
- **Recommended Camera**: iPhone, AV Camera
- **Image Types / Scenarios**:
  - Walking, standing, or running
  - Different distances: close, medium, far
  - Partially occluded
  - Different lighting and background scenarios

## 2. QCar
- **Class ID**: 2  # Same as "car" in COCO dataset
- **Number of Images**: 500 - 1000
- **Recommended Camera**: iPhone for diverse angles, AV Camera for real driving scenarios
- **Image Types / Scenarios**:
  - Front, side (left/right), rear view
  - Different distances
  - Partial occlusion (e.g., other cars, pedestrians)
  - Various backgrounds: urban streets, parking lots, highways
  - Different lighting: daytime, nighttime, shadows
  - Different weather conditions: sunny, cloudy, rainy

## 3. Road Signs
- **Class ID**: 3  # Generic road signs
- **Number of Images**: 300 - 600
- **Recommended Camera**: iPhone, AV Camera
- **Image Types / Scenarios**:
  - Front-facing signs
  - Angled/perspective view
  - Different distances
  - Different lighting: day, dusk, night
  - Partially occluded by trees, poles, or other objects
  - Different environments: urban, suburban, highways

## 4. Stop Sign
- **Class ID**: 7
- **Number of Images**: 300 - 600
- **Recommended Camera**: iPhone, AV Camera
- **Image Types / Scenarios**:
  - Front-facing and angled view
  - Different distances
  - Different lighting: day, dusk, night
  - Partially occluded
  - Urban, suburban, highway backgrounds

## 5. Yield Sign
- **Class ID**: 8
- **Number of Images**: 200 - 400
- **Recommended Camera**: iPhone, AV Camera
- **Image Types / Scenarios**:
  - Front-facing and angled view
  - Different distances
  - Day/night lighting
  - Partially occluded

## 6. Traffic Lights
- **Class IDs**: 4 (Red), 5 (Yellow), 6 (Green)
- **Number of Images**: 400 - 800 per color
- **Recommended Camera**: iPhone, AV Camera
- **Image Types / Scenarios**:
  - Front and angled view
  - Different distances
  - Daytime and nighttime
  - Occluded or partially blocked lights
  - Hanging or pole-mounted types
  - Various backgrounds: intersections, highways, urban streets

## Additional Notes
- Each image should ideally contain **at least one object of interest**.
- Bounding boxes should **fully cover the object**; exact perfection is not required.
- Use diverse environments and conditions to improve model robustness.
- Optionally, use **Segment Anything Model (SAM)** to generate initial masks for segmentation.
- Balance between iPhone and AV Camera images to improve generalization and real-world performance.
