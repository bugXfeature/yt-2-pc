# YT Downloader

A sleek, locally-hosted web application to download YouTube videos and audio at the highest available quality. 

Built with a Python/Flask backend and a modern, responsive front end, this tool bypasses YouTube's stream separation by downloading high-resolution video and audio streams independently and merging them locally.

## ✨ Features

* **High-Quality Video:** Automatically fetches and merges the best available video (up to 4K/1080p) and audio streams.
* **Audio-Only Mode:** Option to extract and download just the audio as an MP3.
* **Dynamic Quality Selector:** Fetches available resolutions for a specific video before downloading.
* **Modern UI:** A beautiful, responsive dark-mode interface featuring a grid aesthetic, built with pure HTML/CSS.
* **Browser Integration:** Automatically opens the app in your default web browser upon launch.

## 🛠️ Tech Stack

* **Backend:** Python, [Flask](https://flask.palletsprojects.com/)
* **YouTube Engine:** [pytubefix](https://pypi.org/project/pytubefix/) (a reliable fork of pytube)
* **Video Processing:** [MoviePy](https://zulko.github.io/moviepy/) (for merging video and audio streams)
* **Frontend:** HTML5, CSS3, Vanilla JavaScript (Fonts: Syne & JetBrains Mono)

## 🚀 Installation & Setup

### Prerequisites
Make sure you have **Python 3.8+** installed on your system. 

### 1. Clone the repository
```bash
git clone https://github.com/bugXfeature/yt-2-pc.git
cd yt-2-pc
```

### 2. Set up a virtual environment (Recommended)
```bash
python -m venv venv
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

*(Note: `moviepy` handles video merging. If you encounter codec errors during the merging process, ensure you have FFmpeg installed on your system, though `imageio-ffmpeg` usually handles this automatically).*

## 💻 Usage

Start the Flask server by running the main Python script:

```bash
python app.py
```

The application will automatically launch your default web browser and navigate to `http://127.0.0.1:5000`. 

1. Paste a valid YouTube URL into the input field.
2. Click **Fetch** to retrieve the video title and available qualities.
3. Select your desired format (Video or Audio) and resolution.
4. Click **Download**. The server will process the video and push the final file to your browser's default download folder.

## 📁 Project Structure

```text
yt-downloader/
│
├── app.py               # Main Flask application and download logic
├── requirements.txt     # Python dependencies
└── templates/
    └── index.html       # Frontend user interface
```

## ⚠️ Disclaimer

This tool is for educational and personal use only. Please respect YouTube's Terms of Service and the copyright of content creators. Do not download content without permission.
```
