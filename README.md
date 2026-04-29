# Gaze-Controlled Wheelchair System
A computer vision-based system that allows users to control a wheelchair using eye movements and blinking. This project uses real-time webcam input to detect gaze direction and sends commands to a hardware device (Arduino/ESP) via serial communication.

## Features
- Real-time eye gaze detection (Left / Right / Center)  
- Blink detection for triggering actions  
- Live webcam processing using OpenCV  
- Serial communication with Arduino/ESP  
- Hands-free wheelchair control  

## Tech Stack
- Python  
- OpenCV  
- GazeTracking Library  
- cvzone  
- PySerial  

## How It Works
1. Webcam captures real-time video  
2. Frames are processed using gaze tracking  
3. System detects:
   - Looking left  
   - Looking right  
   - Looking center  
   - Blinking  
4. Commands are sent to the connected hardware device  

## Project Structure
```
project/
├── main.py
├── Try.py
```

## Hardware Requirements
- Webcam  
- Arduino / ESP module  
- USB Serial connection  

## Installation
```
pip install opencv-python
pip install gaze-tracking
pip install cvzone
pip install pyserial
```
## Run the Project
```
python main.py
```

## Configuration
Update the serial port in your code:

```
esp = SerialObject('/dev/cu.usbserial-XXXX', 115200)
```
### Change according to your system:
- Windows → COM3, COM4  
- Mac/Linux → /dev/tty...  

## Logic Summary
- Blink → Move forward  
- Look left → Turn left  
- Look right → Turn right  
- Look center → Stop  
