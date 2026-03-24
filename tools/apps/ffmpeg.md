# ffmpeg

A complete, cross-platform solution to record, convert and stream audio and video.

## Installation

```shell
sudo apt install ffmpeg -y
```

## Usage

Extract subtitle from a mkv file using `-map` to select the first subtitle stream (`0:s:0`):

```shell
ffmpeg -i video.mkv -map 0:s:0 subs.srt
```

Probe media file metadata with `ffprobe`:

```shell
ffprobe video.mkv
```

Play media file directly with `ffplay`:

```shell
ffplay video.mkv
```

### Related links

- [ffmpeg by example](https://ffmpegbyexample.com/)
- [How to extract subtitle from video using ffmpeg?](https://superuser.com/questions/583393/how-to-extract-subtitle-from-video-using-ffmpeg)

## References

- [ffmpeg](https://ffmpeg.org/)
- [ffmpeg GitHub](https://github.com/FFmpeg/FFmpeg)
