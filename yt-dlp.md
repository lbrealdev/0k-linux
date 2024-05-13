# yt-dlp


Install `yt-dlp` using pip 
```shell
pip install yt-dlp
```

## Facebook

Download from Facebook:
```shell
yt-dlp https://www.facebook.com/user.fb/videos/4024873453531941/ --add-header 'cookie: datr=hZk-ZK5k223rd23cxda; sb=kJk-ZBiY0JZ2342dsdfcs3-; c_user=100010323256897; m_ls=%7B%22c%22%3A%7B%221%22%3A%22HCwAABb0_wcW-qKn4wITBBbi47a3sr0tAA%22%2C%AFsLHjMQMFgAAFigA%22%7D%2C%22d%22%3A%22324d893a-48fd-450b-aef7-2af6ad7c1c89%22%2C%22s%22%3A%220%22%2C%22u%22%3A%22n1w2x2%22%7D; oo=v1; fr=1dVYjqxfwMfdF8oI7.AWUTzCoGf9V6PP69rmFlp4qOGKM.Blc2RV.d1.AAA.0.0.BlqsK4.AWXGFa-TXlI; xs=48%3AWhRdRB198YvUqA%3A2%3A1681824145%3A-1%3A3188%3A%3AAcW8QColFE0NukB1hnaknVSi1SFED; presence=C%7B%22t3%22%3A%5B87425%2C%22v%22%3A1%7D; wd=1920x621'
```

Download from Facebook loading cookies from chrome:
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
yt-dlp -o '%(title)s-%(id)s.%(ext)s' --get-description -f b <youtube-video-url>
```

**Source**: https://github.com/yt-dlp/yt-dlp
