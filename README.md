PoseDetection with YOLOv8: Hand Detection and Pose Estimation

This repository provides a Python script for performing pose detection using the YOLOv8 model. It detects human poses and extracts the coordinates of the left and right hands from images. The keypoints are visualized, and the hand coordinates are saved in a JSON file for further use.

Requirements
•	Python 3.x
•	cv2 (OpenCV)
•	matplotlib
•	json
•	ultralytics (for YOLOv8)

You can install the necessary dependencies by running:

pip install opencv-python matplotlib ultralytics


How It Works
The script uses the YOLOv8 Pose model to detect human poses in an image. After detecting the pose, it identifies the keypoints corresponding to the left and right hands and marks them with blue circles. The coordinates of these keypoints are extracted and saved in a JSON file.

Key Features:
•	Pose Detection: Detects human poses in images using the YOLOv8 model.
•	Hand Detection: Extracts and visualizes the positions of the left and right hands from detected poses.
•	Image Annotation: Draws keypoints and skeletons on the image for visual inspection.
•	JSON Output: Saves the detected hand coordinates to a JSON file.

Usage

Class Overview
The main functionality is encapsulated in the PoseDetection class, which provides the following methods:
1.	__init__(self, model_path): Initializes the pose detection model with the path to the YOLOv8 model.
2.	perform_pose_detection(self, image_path): Loads the input image and performs pose detection using the YOLOv8 model.
3.	draw_annotated_image(self, results, image): Annotates the image with detected keypoints and skeletons.
4.	get_hand_coordinates(self, results, image): Extracts the coordinates of the left and right hands and draws them on the image.
5.	save_coordinates_to_json(self, coordinates, output_path): Saves the extracted hand coordinates into a JSON file.
6.	display_image(self, image, figure_size=(10, 6)): Displays the image using Matplotlib.

Example Output:
1.	Annotated Image: The image with keypoints and skeletons drawn on it, including blue circles marking the left and right hands.
2.	Hand Coordinates JSON: A JSON file containing the coordinates of the detected left and right hands.

Installation
1.	Clone the repository or download the Python script.
2.	Install the required dependencies (listed above).
3.	Download the YOLOv8 Pose model (yolov8n-pose.pt) and place it in the project directory.

Notes
•	Image Input: Make sure to replace test_image_2.jpg with the path to your own input image for pose detection.
•	Model Path: Ensure that you have the correct YOLOv8 pose model file (yolov8n-pose.pt) available in the same directory or specify the correct path.
