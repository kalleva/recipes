## Simple compression:

```ffmpeg -i input.mp4 -vcodec libx265 -crf 28 output.mp4```

## 1080p to 720p more agressive

### Portrait

```ffmpeg -i input.mp4 -vcodec libx265 -crf 32 -vf scale=720:1280 output_720.mp4```

### Landscape

```ffmpeg -i input.mp4 -vcodec libx265 -crf 32 -vf scale=1280:720 output_720.mp4```

