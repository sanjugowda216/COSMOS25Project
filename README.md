# COSMOS25Project
DIRECTIONS

GIT COMMANDS
- always git pull
- NEVER COMMIT TO MAIN - checkout new branch with "git checkout -b branchName"
- git add .
- git commit -m "your message"
- git push origin branchName



📁 models/

Purpose: Load and manage your pretrained models
	•	depth_model.py
	•	Loads your depth estimation model (e.g., MiDaS or Depth Anything)
	•	Preprocesses images for input
	•	Returns a depth map from an image
	•	object_model.py
	•	Loads your object detection model (YOLOv8 or Grounding DINO)
	•	Runs detection on an image and returns bounding boxes + labels

⸻

📁 scripts/

Purpose: Contains the core logic for running/testing parts of your system
	•	main_pipeline.py
	•	The main real-time pipeline that ties everything together
	•	Captures webcam input
	•	Gets depth + object detections
	•	Matches objects with their depth
	•	Triggers audio alert for close objects
	•	depth_only.py
	•	Test script to run only the depth model
	•	Verifies the model works and outputs correct depth map
	•	detect_only.py
	•	Test script to run only the object detection model
	•	Useful for trying out images or tuning detection accuracy
	•	tts_test.py
	•	Simple script to test text-to-speech
	•	Helps verify your TTS engine works and sounds good

⸻

📁 utils/

Purpose: Helper functions to keep your code clean and modular
	•	preprocessing.py
	•	Functions for resizing and preparing images for the models
	•	For example, normalization, resizing, etc.
	•	overlay_utils.py
	•	Drawing functions to display bounding boxes, labels, depth maps
	•	Optional: blend depth + object detection on-screen

⸻

📁 assets/

Purpose: Demo visuals and outputs
	•	example_output.jpg / demo.gif / demo_video.mp4
	•	Screenshots or short clips showing the system in action
	•	Useful for your poster and GitHub README

⸻

📄 requirements.txt
	•	A list of Python packages your project depends on
	•	Makes it easy for others to install everything with pip install -r requirements.txt

⸻

📄 README.md
	•	Overview of your project: what it does, how to run it, sample outputs
	•	Include:
	•	Project description
	•	Setup instructions
	•	How to run main pipeline
	•	Team member credits
	•	Screenshots or demo link

⸻

📄 .gitignore
	•	Tells GitHub to ignore files like:
	•	Model checkpoints (YOLO, MiDaS)
	•	Cache files
	•	Personal editor files (e.g. .vscode/, __pycache__/)
