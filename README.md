# Basketball Analysis

This project is an **automated basketball video analysis system** designed to extract meaningful insights from basketball game footage without manual annotation. It combines advanced computer vision techniques, object detection, tracking, and event recognition to provide a full, annotated view of a basketball game.

### **What the project does**

1. **Player and Ball Detection**
   - Uses YOLO-based models to detect all players and the ball in every frame.
   - Each player and the ball is localized with bounding boxes for accurate tracking.

2. **Player Tracking**
   - Tracks each player across frames, assigning consistent IDs even during fast movements or overlaps.
   - Ensures stable identification of each player throughout the game.

3. **Team Assignment**
   - Differentiates players into two teams based on jersey color.
   - Uses color-based analysis and zero-shot classification for reliable team assignment.
   - Incorporates temporal smoothing to maintain consistent team IDs across frames.

4. **Event Detection**
   - **Ball possession:** Identifies which player has the ball at any given time.
   - **Pass detection:** Detects passes between players.
   - **Interception detection:** Detects when the opposing team intercepts the ball.

5. **Court Keypoint Detection**
   - Detects keypoints on the basketball court, such as lines, corners, and important zones.
   - Provides spatial context to understand player positions and movements relative to the court.

6. **Visualization**
   - Overlays all detected elements (players, ball, passes, court lines) onto video frames.
   - Produces a fully annotated video that clearly visualizes game dynamics and events.

### **Why this project is useful**

- Automates the manual process of analyzing basketball games.
- Helps coaches and analysts study player movements, team strategies, and game events efficiently.
- Provides a foundation for further sports analytics, such as performance metrics, tactical analysis, and AI-driven insights.
- Can be extended for real-time analysis, additional events, or advanced metrics like player speed, distance, and heatmaps.

---

### **Technical Highlights**

- **Programming Language:** Python 3.8+  
- **Detection Models:** YOLOv5, YOLOv8 (Ultralytics)  
- **Tracking Algorithms:** Multi-object tracking with bounding boxes, optional Kalman filtering  
- **Dataset Management:** Roboflow  
- **Visualization:** OpenCV-based drawing of bounding boxes, keypoints, passes, and court lines  
- **Modular Structure:** Separate modules for detection, tracking, team assignment, event detection, and visualization  
