# rotate video

without reencoding
``ffmpeg -i input.mp4 -metadata:s:v:0 rotate=90 -c copy output.mp4``

reencoding
``ffmpeg -i input.mp4 -vf "rotate=90" output.mp4``
