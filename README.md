Football Game Analysis with YOLOv8 and Computer Vision
This project leverages YOLOv8 and custom object detection techniques to analyze football games, focusing on detecting players, referees, and footballs. It also includes features for tracking player movement, assigning players to teams based on t-shirt colors, and calculating speed and distance using optical flow and perspective transformation.

Features
YOLOv8 Object Detection: Detect players, referees, and footballs in images and videos.
Custom YOLO Model: Fine-tune and train your own YOLOv8 model on custom datasets for improved detection.
Player Team Assignment: Use KMeans clustering for pixel segmentation to assign players to teams based on t-shirt colors.
Movement Tracking: Measure camera movement using optical flow.
Perspective Transformation: Calculate player movement in meters rather than pixels.
Speed and Distance Calculation: Track player speed and the distance covered in the game.
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/football-game-analysis.git
cd football-game-analysis
Install the required dependencies:

bash
Copy code
pip install -r requirements.txt
Download the YOLOv8 model:

bash
Copy code
python -m ultralytics.yolo.v8
Usage
Detect objects in videos:

bash
Copy code
python detect.py --input your_video.mp4 --output output_video.mp4
Train custom YOLOv8 model:

bash
Copy code
python train.py --data your_dataset.yaml --cfg yolov8.yaml
Segment players and calculate movement:

bash
Copy code
python segment_and_track.py --input your_video.mp4
Key Concepts
YOLOv8: A state-of-the-art real-time object detector.
KMeans Clustering: Used for t-shirt color segmentation to assign players to teams.
Optical Flow: Used to measure camera movement between frames.
Perspective Transformation: Adjusts the scene’s depth to calculate real-world player movement in meters.
