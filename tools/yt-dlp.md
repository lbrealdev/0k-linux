# yt-dlp

Install `yt-dlp` using pip 
```shell
pip install yt-dlp
```

## Facebook

Download from Facebook loading cookies from chrome browser:
```shell
yt-dlp https://www.facebook.com/watch/?v=<facebook-video-id> --cookies-from-browser chrome
```

If you get any errors when downloading with `--cookies-from-browser`, you should install the `secretstorage` module and run again:
```shell
python3 -m pip install secretstorage
```

**NOTE:** Follow the steps in the answer from `stackexchange webapps`.

- https://webapps.stackexchange.com/a/92332


## YouTube

Get a list of formats available for download:
```shell
yt-dlp --list-formats <youtube-video-url>
```

Download all playlists from a YouTube channel:
```shell
yt-dlp -o '%(title)s-%(id)s.%(ext)s' -f b --yes-playlist https://www.youtube.com/c/<youtube-channel-name>
```

Download the video with the best quality and description:
```shell
yt-dlp -o '%(title)s-%(id)s.%(ext)s' --write-description --embed-metadata -f b <youtube-video-url>
```

List all videos from YouTube channel:
```shell
yt-dlp --print "%(title)s-%(id)s" https://www.youtube.com/@<uploader_id> > youtube-videos-list.txt
```

## Twitter

Download video from Twitter:
```shell
yt-dlp <twitter-video-address>
```

**Source**: https://github.com/yt-dlp/yt-dlp
