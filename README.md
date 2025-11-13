# Webcam OSC Grid Analyzer

A Python application that captures webcam video, analyzes each region of the frame, and sends the data via OSC (Open Sound Control) for real-time audiovisual interaction.

## Purpose

This project enables real-time video analysis and OSC communication for creative coding, interactive installations, audiovisual performances, and multimedia projects. It analyzes each grid cell for:

- Average RGB color values
- Brightness levels
- Contrast measurements
- Dominant colors

The analyzed data is transmitted via OSC protocol, making it compatible with software like Max/MSP, TouchDesigner, Processing, Pure Data, and other creative coding environments.

## Pure Data Integration

The project includes a Pure Data patch named brightness_sound_maker.pd, which receives OSC data from the Python script. The patch uses the incoming camera information to generate sound in real time:

- Brightness controls an increasing rhythmic beat, similar to a club-style pulse.

- Red channel (R in RGB) controls the volume of the beat.

In summary, brightness shapes the rhythm, and the red intensity determines its loudness.

## How It Works

1. **Video Capture**: Captures frames from your webcam at a configurable frame rate
2. **Grid Division**: Divides each frame into a configurable grid (default: 4x4)
3. **Cell Analysis**: Analyzes each grid cell for color, brightness, contrast, and dominant color
4. **OSC Transmission**: Sends analyzed data to a specified host and port via OSC protocol
5. The data is sent through OSC to a chosen host and port.
6. Pure Data receives the OSC messages and produces sound based on them.
7. A live preview with a grid overlay is displayed.

