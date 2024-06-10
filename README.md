# ESP32-4827A043

## RED Board

Board: ESP32S3 Dev Module
USB CDC On Boot: Disabled
Flash Size: 16MB
PSRAM: OPI PSRAM

## BLACK Board

Board: ESP32S3 Dev Module
USB CDC On Boot: Enabled
Flash Size: 16MB
PSRAM: OPI PSRAM

## AVI conversion

### Cinepak

```sh
ffmpeg -i input.mp4 -c:a mp3 -c:v cinepak -q:v 20 -vf "fps=15,scale=-1:272:flags=lanczos,crop=480:272:(in_w-480)/2:0" AviMp3Cinepak272p15fps.avi
```

### MJPEG

```sh
ffmpeg -i input.mp4 -c:a mp3 -c:v mjpeg -q:v 10 -vf "fps=15,scale=-1:272:flags=lanczos,crop=480:272:(in_w-480)/2:0" AviMp3Mjpeg272p15fps.avi
```


## MPEG conversion

```sh
ffmpeg -i input.mp4 -c:v mpeg1video -vb 320k -c:a mp2 -ab 64k -vf "fps=25,scale=-1:240:flags=lanczos,crop=320:240:(in_w-320)/2:0" -y 320x240.mpg
```
