# AI Image Generation Pipeline

A complete desktop application that automates AI image generation from text prompts. Upload a Word document, click a button, and watch AI generate images automatically!

## Demo

1. Open the app
2. Upload a Word document with prompts (one per line)
3. Click Run Pipeline
4. Watch images generate in real time
5. View all images in the built-in gallery

## What It Does

1. Reads .docx files from your computer
2. Extracts text prompts from the document (supports multiple prompts)
3. Generates an AI image for each prompt using Pollinations AI (free, no API key needed)
4. Embeds all generated images back into the same Word document
5. Saves images locally to your computer
6. Tracks files across Google Drive folders (inbox, processing, done)

## Features

- Desktop GUI app with dark sidebar and light content area
- Upload and run pipeline with one click
- Real time log showing pipeline progress
- Image gallery to view all generated images
- File status tracker showing Google Drive folder contents
- Supports multiple prompts in one document
- Double click launcher (no Command Prompt needed)

## Screenshots

Upload and Run
- Browse and select your Word document
- Click Run Pipeline
- Watch real time logs as images are generated

Image Gallery
- View all generated images in a grid layout
- Scrollable gallery

File Status
- See all files in inbox, images and done folders on Google Drive

## Project Structure

ai-image-pipeline/
├── app.py                  # Desktop GUI
