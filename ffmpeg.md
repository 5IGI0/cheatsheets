# rotate video

without reencoding
``ffmpeg -i input.mp4 -metadata:s:v:0 rotate=90 -c copy output.mp4``

reencoding
``ffmpeg -i input.mp4 -vf "rotate=90" output.mp4``

# compress video

specific bitrate
``ffmpeg -i input.mp4 -b:v <video bitrate (kb)>k -b:a <audio bitrate (kb)>k output.mp4`` (note: in kilobit, not kilobyte)

crf
``ffmpeg -i input.mp4 -crf <loss level> output.mp4``
(higher value = more loss = smaller, generally 32 is the default)

# truncate video

by size
``ffmpeg -i input.mp4 -fs <size in byte> output.mp4``

by duration
``ffmpeg -i input.mp4 -t <duration> output.mp4``

by duration (without rencoding (might break some players)) \
``ffmpeg -t <duration> -i input.mp4 output.mp4``

