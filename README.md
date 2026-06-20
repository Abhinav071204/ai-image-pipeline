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
├── app.py                  # Desktop GUI application
├── pipeline.py             # Command line pipeline script
├── config.py               # Your private settings (not uploaded)
├── LaunchPipeline.bat      # Double click to launch the app
├── requirements.txt        # Required Python packages
├── .gitignore              # Keeps private files off GitHub
└── README.md               # Project documentation

## Technologies Used

- Python 3
- Tkinter (Desktop GUI)
- Google Drive API
- Google Cloud Service Account
- Pollinations AI (free image generation)
- python-docx (Word document processing)
- Pillow (Image processing)

## Setup Instructions

### 1. Clone the repository
git clone https://github.com/Abhinav071204/ai-image-pipeline.git

### 2. Install required packages
pip install -r requirements.txt

### 3. Set up Google Cloud
- Create a Google Cloud project
- Enable the Google Drive API
- Create a Service Account and download the JSON key
- Create 3 folders on Google Drive: inbox, images, done
- Share all 3 folders with the service account email

### 4. Create your config.py
Create a config.py file in the project folder:

KEY_PATH = path to your service account JSON key file
LOCAL_OUTPUT = path to save images locally on your computer
FOLDERS = your Google Drive folder IDs for inbox images and done

### 5. Launch the app

Option A - Double click:
Double click LaunchPipeline.bat on your Desktop

Option B - Command Prompt:
python app.py

## How to Use

1. Create a Word document (.docx) with one prompt per line example:
   a cat sitting on a mountain at sunset
   a dog running on a beach
   a dragon flying over a castle

2. Open the app by double clicking LaunchPipeline.bat
3. Click Browse File and select your Word document
4. Click Run Pipeline
5. Watch images generate in real time in the log
6. Click Image Gallery to see all generated images
7. Open the output Word document to see images embedded inside

## Resume Description

Designed and built an end-to-end AI image generation desktop application using Python. The app reads text prompts from Word documents, generates AI images using Pollinations API, embeds generated images back into the source document, and includes a built-in image gallery and Google Drive file status tracker — reducing manual effort to zero.

## GitHub

https://github.com/Abhinav071204/ai-image-pipeline
