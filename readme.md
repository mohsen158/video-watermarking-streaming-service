Build Live Video Streaming with watermarking Server use Ffmpeg Nginx Rtmp Module  

## Pre-Document
+https://github.com/tabvn/video-streaming-service
+
+



## Setup Nginx + Nginx-rtmp-module & Ffmpeg 
```
sudo apt-get 

instal nginx-full

```

## FFMPEG streaming
```
ffmpeg -re -i video.mkv -c:v libx264 -preset veryfast -maxrate 3000k -bufsize 6000k -pix_fmt yuv420p -g 50 -c:a aac -b:a 160k -ac 2 -ar 44100 -f flv rtmp://localhost/live/play
```

## FFMPEG streaming with watermark
```
ffmpeg -re -i hls/index.m3u8  -i neolej.png -filter_complex "overlay=10:10"    -c:v libx264 -preset veryfast -maxrate 3000k -bufsize 6000k -pix_fmt yuv420p -g 50 -c:a aac -b:a 160k -ac 2 -ar 44100 -f flv rtmp://localhost/play
```

## Nginx Config Sample for Nginx + Nginx Rtmp Module
in nginx.conf file 

## heml sampling page for video streaming 

in index.html file 
