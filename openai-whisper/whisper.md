## create and activate a python virtual environment
```
python3 -m venv .venv
source .venv/bin/activate
```

## Install FFmpeg (required for audio handling)


```
sudo apt update
sudo apt install ffmpeg
```


## Install whisper
```
pip install -U openai-whisper
```


# run whisper

```
whisper "your_audio_file.mp3" --model base --output_format txt
```
