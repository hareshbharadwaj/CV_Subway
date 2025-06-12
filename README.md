# CV_Subway

🕹️ Hand Gesture Controller for Subway Surfers (Webcam + Python + Mediapipe)
Control Subway Surfers or any PC game using your hand gestures via webcam!
This project tracks your hand using MediaPipe and allows you to:

Swipe left/right/up/down by hand motion,

Trigger Skateboard (Jump) by making a fist twice,

Pause/Resume the game when your hand goes outside/inside a circle overlay.

📦 Features
✅ Real-time hand tracking with MediaPipe

🎮 Keyboard emulation using pyautogui

🧭 Joystick-style interface overlay

✊ Double fist = Skateboard

⏸ Auto-pause when hand moves outside control area

🖥️ Always-on-top joystick window (Windows only)

🧰 Requirements
Python 3.7+

OpenCV

MediaPipe

PyAutoGUI

Windows OS (for always-on-top window)

Install dependencies:

pip install opencv-python mediapipe pyautogui
🚀 How to Run
Launch Subway Surfers using Bluestacks or any other emulator.

Open the terminal and run:

python subway.py
A window with a circle and arrow UI will appear (acts like a virtual joystick).

Keep your hand inside the circle and move:

👉 Right → Right arrow

👈 Left → Left arrow

👆 Up → Up arrow

👇 Down → Down arrow

Make a fist twice quickly → 🛹 Presses Space to activate skateboard.

Move hand outside the circle → ⏸ Pauses the game (sends P key).

Bring hand back inside → ▶️ Resumes the game.

🧠 How It Works
Hand Detection: Uses MediaPipe to detect hand landmarks.

Direction Detection: Calculates movement vector and detects swipes.

Fist Detection: Calculates thumb-index distance for a closed hand.

Joystick Overlay: Displays circle with directional arrows.

Keyboard Input: Sends keys using pyautogui.press() based on gestures.

Auto Pause: If the hand leaves the control circle, pauses the game.

Always-on-top: Keeps the control window on top using ctypes (Windows).

🎯 Controls Summary
Gesture	Action	Key Sent
Move hand right	Move Right	→
Move hand left	Move Left	←
Move hand up	Jump	↑
Move hand down	Roll	↓
Double Fist (quickly)	Skateboard Jump	Space
Hand outside joystick area	Pause Game	P
Hand inside joystick area	Resume Game	P
📝 Notes
Adjust joystick_radius, gesture_cooldown, or fist_threshold for sensitivity.

Works best with a plain background and good lighting.

Use full-screen mode for emulator but keep the control window visible.

