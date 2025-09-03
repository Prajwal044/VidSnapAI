# VidSnapAI 
vidsnapai is a web application that lets users create stunning TikTok-style reels by uploading images, writing captions, and generating lifelike voiceovers using ElevenLabs AI. Automatic video stitching and music integration make content creation instant and effortless.

## Features
- **User UUIDs**: 
Each user receives a unique identifier generated with Python’s uuid library for secure file tracking and personalization.

- **Image Upload**: Seamlessly upload multiple images to form the visual foundation of the reel.

- **Caption to Voice**: Captions are transformed into realistic audio by ElevenLabs' API, creating engaging voiceovers for each video.

- **Background Music**: Optionally add music tracks for greater creative control.

- **Automatic Video Assembly**: Images, generated audio, and music are stitched together to produce social-ready videos.

- **Responsive, Stylish UI**: Built with Flask, HTML, CSS, Jinja, and Bootstrap for an intuitive, attractive interface.

## How It Works
- The web application is built using Flask, a lightweight Python web framework that handles HTTP requests, routing, and rendering HTML templates.

- When a user interacts with the app, Flask generates a unique user identifier (UUID) using Python’s uuid library to uniquely track each user's session and media files securely.

- Users upload images, and filenames are sanitized using werkzeug.utils.secure_filename to prevent security issues during file storage on the server.

- Uploaded images, user captions, and other data are processed through Flask routes that handle file uploads, form submissions, and background tasks.

- Captions submitted by the user are converted into audio using ElevenLabs’ API (integrated separately) and saved as audio files.

- The server then stitches the images and generated audio (caption voice + optional music) into a seamless video using Python media libraries or command-line tools invoked via subprocess.

- The frontend interface is rendered using Jinja2 templates with HTML, styled by Bootstrap and CSS for a responsive and user-friendly experience.

## Tech Stack
- **Backend Framework**: Flask (Python) — Handles routing, user sessions (UUID), file uploads, and API integration.

- **Unique ID Generation**: Python’s uuid standard library — Ensures unique user and session identifiers.

- **File Handling**: Flask + werkzeug.utils.secure_filename for secure file uploads.

- **Frontend Rendering**: Jinja2 templating engine to dynamically generate HTML pages.

- **Frontend Styling**: Bootstrap CSS and custom CSS for responsive, clean UI design.

- **Audio Generation**: ElevenLabs API for text-to-speech conversion of user captions.

- **Media Processing**: Python libraries (e.g., MoviePy) or external tools executed via subprocess for video creation.

- **Operating System Interface**: os library for managing file paths and system operations.