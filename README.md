This project demonstrates real-time human detection using the ESP32-CAM (AI-Thinker) and a model trained via Edge Impulse. It captures camera frames, runs inference on-device, and prints results to the serial monitor.

🧠 Powered by
Edge Impulse - For building and deploying the ML model
ESP32 Arduino Core v2.0.4
OV2640 camera (AI-Thinker module)

📦 Requirements
ESP32-CAM (AI-Thinker)
Arduino IDE with ESP32 board manager (v2.0.4 recommended)
Edge Impulse trained model with object detection support
Serial Monitor (115200 baud)

🔧 Setup
1. Install Dependencies
Install Arduino IDE
Add ESP32 Board to Board Manager (version 2.0.4)
Install the following libraries:
esp_camera.h
Edge Impulse Inferencing SDK (auto-included in exported model)

2. Connect ESP32-CAM
Wire it to FTDI as follows:
ESP32-CAM Pin	FTDI
GND	GND
5V	VCC
U0R	TX
U0T	RX
IO0	GND (during upload only)

3. Upload Firmware
Select board: AI Thinker ESP32-CAM
Baud Rate: 115200
Upload the code from main.cpp

🚀 How It Works
Camera Initialization
The ESP32-CAM is configured to use the OV2640 sensor at QVGA resolution.

📷 Supported Camera Models
CAMERA_MODEL_AI_THINKER (default in code)
You can also switch to CAMERA_MODEL_ESP_EYE by uncommenting in main.cpp.

📌 Notes
Ensure good lighting for reliable detection.
PSRAM is required — use modules with built-in PSRAM like AI-Thinker.
