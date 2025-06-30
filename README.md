Created by ME Suvhankar Dutta
Component	Details
Webcam Input	cv2.VideoCapture(0) starts webcam stream
Hand Detection	mediapipe.solutions.hands detects hand landmarks (21 per hand)
Gesture Tracking	Monitors distance between thumb tip (id=4) and index tip (id=8)
Volume Mapping	Maps hand distance (30–200 px) to system volume range using np.interp()
Audio Control	Uses pycaw to set volume with SetMasterVolumeLevel()
Visual Feedback	Shows circles, a line between fingers, and a volume bar on the video frame
Exit Condition	Pressing q key stops the program

Thumb tip (ID 4) and Index tip (ID 8) are tracked.
The distance between these two points is used to adjust system volume.
A short distance = low volume, and a large distance = high volume.
A volume bar is drawn on the screen to show visual feedback.

