This project is a hand gesture-based virtual mouse system using a webcam and computer vision. It uses MediaPipe for real-time hand tracking, OpenCV for image processing, and PyAutoGUI/Pynput for controlling mouse actions. Here's a breakdown of its features and how it works:

🖐️ Project Description: Hand Gesture Virtual Mouse Controller

The project enables users to control the computer mouse using hand gestures captured by a webcam. It detects specific gestures to perform common mouse functions such as moving the cursor, left click, right click, double click, and taking a screenshot — all without touching the mouse.

🔧 Technologies Used:

MediaPipe – For detecting and tracking hand landmarks.

OpenCV – For image capture, processing, and UI display.

PyAutoGUI – For controlling the mouse pointer and automating actions.

Pynput – For more precise mouse click simulation.

NumPy – For mathematical operations like angle and distance calculation.

🧠 How It Works:
Hand Detection and Landmark Extraction:

MediaPipe identifies 21 hand landmarks.

These landmarks are used to determine finger positions and gestures.

Mouse Movement:

Moving the index finger while thumb and index are close (distance < 50) moves the mouse pointer proportionally on the screen.

Gesture Recognition: Gestures are interpreted using geometric calculations:

Left Click: Index finger bent (low angle), middle finger up, thumb away.

Right Click: Middle finger bent, index finger up, thumb away.

Double Click: Both index and middle fingers bent, thumb away.

Screenshot: Both index and middle fingers bent, thumb close to index.

Visual Feedback:

The corresponding action text (like "Left Click", "Screenshot Taken") is overlaid on the video feed.

🖱️ Mouse Functions Mapped to Gestures:

Gesture	Action
Index finger movement	Move mouse
Index bent + thumb far	Left Click
Middle bent + thumb far	Right Click
Both bent + thumb far	Double Click
Both bent + thumb near	Take Screenshot
