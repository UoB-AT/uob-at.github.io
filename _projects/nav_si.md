---
layout: project
title: "NavSi: Navigation And Visio-Spatial Information"
author: "Kailey Epstein"
description: "An on device AI-based, multimodal, mobile application to enhance navigation and situational awareness for blind or visually impaired users."
status: "Active"
repo_url: "https://github.com/uob-at/nav-si"
demo_url: "#"
doc_url: "#"
---

## Overview
NavSi (Navigation And Visio-Spatial Information) is a free, open-source, AI-based mobile application designed to enhance situational awareness for blind and visually impaired users. NavSi provides real-time, on-device processing, ensuring user privacy while delivering high-performance environmental feedback.

The system operates entirely through a voice-controlled interface, allowing users to interact with their surroundings without needing to manually operate a screen.

## Key Features
* **Object Detection**: Identifies surroundings and provides specific details, including object position (spatial awareness) and color.
* **Text Detection**: Locates text in the environment and provides positional information to help users navigate signage or documents.
* **Voice-First Interaction**: Fully contactless usage. Users can issue voice commands to switch between detection modes, search for specific items (e.g., "Find my keys"), and request reports on their environment.
* **Privacy-First Design**: All processing runs in real-time on-device, meaning no sensitive image or location data leaves the phone.

## Installation
NavSi is built using the Flutter framework. To run this project locally, clone the repository and set up your environment:

```bash
git clone [https://github.com/uob-at/nav-si](https://github.com/uob-at/nav-si)
cd nav-si
flutter pub get
flutter run