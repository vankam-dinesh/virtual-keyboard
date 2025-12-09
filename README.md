virtual-keyboard ✨ Virtual Gesture Keyboard

A futuristic virtual keyboard powered by hand gestures using MediaPipe, OpenCV, and PyAutoGUI.
Type without touching your keyboard — just move your fingers in front of your webcam!

📸 Features (Enhanced Overview)
🖐️ Gesture-Based Typing

Detects fingertips using MediaPipe Hand Tracking

Tracks finger position to determine which key is “pressed”

Supports both tap and hover based detection

🎨 Modern & Stylish UI

Neon gradient keyboard

Smooth animations

Transparent keyboard overlay

🔠 Smart Shift Toggle

Easily switch between uppercase and lowercase using gesture flicks

📝 Live Typing Window

Displays typed text in real-time

Supports multi-line typing

Auto-scroll enabled

🗂️ Automatic Saving

Everything typed is saved instantly to typed_output.txt

🧾 Instant Notepad Launch

On the first gesture, Notepad opens automatically to show typed text

🖼️ Resizable Window

Keyboard window can be resized (not locked to fullscreen)

🛠 Technologies Used
Technology	Purpose
MediaPipe	Hand-tracking, fingertip detection
OpenCV	Camera input, UI rendering
PyAutoGUI	Simulating key presses
Python 3.x	Core application logic
🚀 How to Run
1️⃣ Clone the repository
git clone https://github.com/vankam-dinesh/virtual-keyboard.git
cd virtual-keyboard

2️⃣ Install dependencies
pip install opencv-python mediapipe pyautogui

3️⃣ Run the virtual keyboard
python virtual_keyboard.py

🗂 Project Structure
virtual-keyboard/
│
├── images/                  # Screenshots and demo images
├── virtual_keyboard.py      # Main gesture keyboard program
├── main.py                  # Alternate runner (optional)
├── typed_output.txt         # Auto-generated typed text
├── README.md                # Project documentation
└── requirements.txt         # Dependencies (optional)

📊 System Flowchart
flowchart TD

A[Start Webcam] --> B[MediaPipe Hand Tracking]
B --> C[Identify Fingertip Coordinates]
C --> D[Map Coordinates to Keyboard Buttons]
D --> E{Gesture Detected?}

E -->|Yes| F[Trigger Key Press Event via PyAutoGUI]
E -->|No| C

F --> G[Display Typed Text on UI]
G --> H[Save to typed_output.txt]
H --> I[Open Notepad (first gesture)]
I --> C

🧠 How It Works (Architecture Breakdown)
1️⃣ Hand Detection with MediaPipe

Uses built-in hand landmark model

Extracts fingertip positions (index & middle finger)

2️⃣ Mapping Finger Positions to Keys

Each keyboard button is a bounding box

If a fingertip enters the box → the key is considered “pressed”

3️⃣ Triggering Key Press

PyAutoGUI simulates the actual typing

Notepad auto-opens on first gesture

4️⃣ Rendering the Keyboard

OpenCV draws the keyboard

Highlights the detected key

Neon-style theme for modern look

5️⃣ Real-Time Output

Text appears instantly on-screen

Also saved continuously in typed_output.txt

📷 Screenshots & Demo

(Add this after uploading your image in the /images folder)

## 🖼 Demo Screenshot
![Gesture Keyboard](images/your-image.png)

🧪 Output Examples
✔ Contents of typed_output.txt
Hello, this is a demo of the virtual gesture keyboard!

✔ Real-time UI shows:

Keyboard layout

Highlighted pressed key

Live typed text preview

🚀 Future Improvements

✋ Add multi-hand support

👆 Add gesture shortcuts (copy, paste, undo)

🎥 Add on-screen gesture trail

🔊 Voice feedback for keypress

📱 Build a GUI-based settings panel

🙌 Contributions

Pull requests are welcome!
Feel free to fork the project and enhance it.

💬 Support

If you like this project, give it a ⭐ on GitHub!
