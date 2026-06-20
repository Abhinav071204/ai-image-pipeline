# AI Image Generation Pipeline

An automated Python pipeline that reads text prompts from Word documents on Google Drive, generates AI images, and embeds them back into the document automatically.

## What It Does

1. Reads .docx files from a Google Drive inbox folder
2. Extracts text prompts from the document (supports multiple prompts)
3. Generates an AI image for each prompt using Pollinations AI (free, no API key needed)
4. Embeds all generated images back into the same Word document
5. Saves images locally to your computer
6. Moves the completed document to a done folder on Google Drive

## Technologies Used

- Python 3
- Google Drive API
- Google Cloud Service Account
- Pollinations AI (free image generation)
- python-docx (Word document processing)

## Project Structure

ai-image-pipeline/
├── pipeline.py       # Main automation script
├── config.py         # Your private settings (not uploaded)
├── .gitignore        # Keeps private files off GitHub
└── README.md         # Project documentation

## Setup Instructions

### 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/ai-image-pipeline.git

### 2. Install required packages
pip install google-api-python-client google-auth-httplib2 google-auth-oauthlib python-docx requests

### 3. Set up Google Cloud
- Create a Google Cloud project
- Enable the Google Drive API
- Create a Service Account and download the JSON key
- Create 3 folders on Google Drive: inbox, images, done
- Share all 3 folders with the service account email

### 4. Create your config.py
Create a config.py file in the project folder with your private settings:

KEY_PATH = path to your service account JSON key
LOCAL_OUTPUT = path to save images locally
FOLDERS = your Google Drive folder IDs for inbox, images and done

### 5. Run the pipeline
python pipeline.py

## How to Use

1. Create a Word document (.docx) with one prompt per line example:
   a cat sitting on a mountain at sunset
   a dog running on a beach
   a dragon flying over a castle

2. Upload it to your inbox folder on Google Drive
3. Run the script
4. Check your done folder on Google Drive for the completed document with images embedded inside

## Resume Description

Designed and built an automated pipeline that monitors a Google Drive inbox folder, extracts text prompts from Word documents, generates AI images using Pollinations AI, embeds generated images back into the source document, and archives completed files reducing manual effort to zero.
