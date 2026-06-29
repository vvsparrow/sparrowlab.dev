# How to download YouTube audio for learning

In 2026, many standard tools for downloading from YouTube are failing due to frequent API changes. To keep my learning process smooth and get audio for my offline practice, I use `yt-dlp`. This is a professional-grade command-line tool.

## 1. Installation
The most reliable way to get the latest version (to avoid HTTP 403 errors) is to download the binary directly from the official GitHub repository:

```
cd ~/Downloads
wget https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_linux
chmod +x yt-dlp_linux
sudo mv yt-dlp_linux /usr/local/bin/yt-dlp
```

## 2. Prerequisites

For audio conversion and high-quality processing, you must have FFmpeg installed on your Linux Mint system:

```
sudo apt update
sudo apt install ffmpeg -y
```

## 3. Recommended Command

To download the best available audio and convert it to a high-quality MP3 (320kbps), use the following syntax:

```
yt-dlp -f bestaudio --extract-audio --audio-format mp3 --audio-quality 0 "URL"
```

## 4. Time-Saving Automation (Bash Alias)

Instead of typing a long command every time, I created an alias. Add this line to your ~/.bashrc file:

```
alias yta='yt-dlp -f bestaudio --extract-audio --audio-format mp3 --audio-quality 0'
```

After restarting your terminal, you can download any lesson by simply typing:

```
yta "https://www.youtube.com/..."
```

This guide is part of my technical journey in Sparrow Lab.
