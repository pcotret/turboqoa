Generate a synthetic sine wave test tone from scratch
```bash
ffmpeg -f lavfi -i "sine=frequency=440:duration=5" -f s16le -ar 48000 -ac 2 test.pcm
```

From an existing audio MP3 file, PCM settings compatible with this tool:
```bash
ffmpeg -i input.mp3 -f s16le -ar 48000 -ac 2 test.pcm
``` 
