Build Live Video Streaming with watermarking Server use Ffmpeg Nginx Rtmp Module  

## Pre-Document
+
+
+



## Setup Nginx + Nginx-rtmp-module & Ffmpeg 
```
sudo apt-get instal nginx-full

```

## FFMPEG used command
ffmpeg -re -i video.mkv -c:v libx264 -preset veryfast -maxrate 3000k -bufsize 6000k -pix_fmt yuv420p -g 50 -c:a aac -b:a 160k -ac 2 -ar 44100 -f flv rtmp://localhost/live/play



## Nginx Config Sample for Nginx + Nginx Rtmp Module
in nginx.conf file 

##heml sampling page for video streaming 
in index.html file 