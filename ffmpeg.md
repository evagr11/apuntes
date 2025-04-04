# ffmpeg

```
ffmpeg -codecs
ffmpeg -formats

ffmpeg -i video.mp4 #informacion del video
ffmpeg -i video.flv -hide_banner
ffprobe -i video.flv -print_format json -hide_banner

ffmpeg -i video_original.avi output.mp4 # convertir
ffmpeg -i youtube.flv -c:v libx264 filename.mp4 # comprimir
ffmpeg -i "concat:video1.mp4|video2.mp4|video3.mp4" -c copy output.mp4 # concatenar videos
ffmpeg -i video.mp4 -ss 00:01:30 -t 00:00:30 -codec copy output.mp4 # extraer un segmento

ffmpeg -i video.mp4 -vn output.mp3 # extraer audio
ffmpeg -i video.mp4 -ss 00:00:30 -vframes 1 output.png # extraer frames
ffmpeg -i video.mp4 -r 0.25 output_%04d.png # combinar imagenes en video
cat *.JPG | ffmpeg -f image2pipe -r 0.3 -vcodec mjpeg -i – -vcodec libx264 output.mp4 # combinar jpeg en video
```
