---
layout: project
title: "AudioTac: Transforming Photographs into Dual-Layer SVGs for Audio-Tactile Interaction"
short_title: "AudioTac"
author: "Juan Pablo Ruiz Partida"
description: "An automated system converting photographs into interactive SVGs for audio-tactile exploration."
timeline: "Jan 2025 – Apr 2025"
association: "University of Bristol"
status: "Completed (BSc Dissertation, 40CP)"
repo_url: "https://github.com/jp-rp/audiotac"
demo_url: ""
doc_url: ""
---

## Overview
AudioTac is an automated system developed to make visual content accessible for blind and low-vision users. The project was submitted as a dissertation for the degree of Bachelor of Science in the Faculty of Engineering at the University of Bristol.

The system combines image segmentation models and Large Language Models (LLMs) to convert everyday photos into interactive SVGs enriched with semantic descriptions. These dual-layer SVGs can be explored through audio feedback using screen readers or tactile displays, broadening access to visual information via a mobile app.

## Key Features
* **AI-Powered Semantic Conversion:** Combines advanced image segmentation models and LLMs to accurately identify and describe everyday photographic elements.
* **Dual-Layer Interactive SVGs:** Translates standard images into structured, interactive vector graphics containing rich semantic metadata.
* **Audio-Tactile Exploration:** Designed to interface seamlessly with screen readers and tactile displays, allowing users to physically or audibly explore visual content.
* **Mobile Application:** Delivers the accessible SVGs directly through a mobile interface, ensuring broad and portable access for users.

## Opportunities for Students
If you are a student interested in working with our lab, AudioTac offers hands-on experience in several cutting-edge fields:
* **Applied Artificial Intelligence:** Work directly with LLMs and segmentation models to solve real-world accessibility problems.
* **Assistive Technology:** Develop solutions for screen readers and tactile displays to make the digital world more inclusive.
* **Full-Stack Application Development:** Gain experience building cross-platform mobile applications (Flutter) linked with powerful backend AI services (Python).

## Installation
To run this project locally, clone the repository and set up the respective backend and frontend environments:

```bash
git clone https://github.com/jp-rp/audiotac.git
cd audiotac

# Backend Setup (Python)
cd backend
pip install -r requirements.txt

# Frontend Setup (Flutter)
cd ../frontend/audiotac
flutter pub get
flutter run
```