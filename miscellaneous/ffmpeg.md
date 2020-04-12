# FFmpeg

#### Mix audio and video from different sources
Mix video of input1 and audio of input2\
<code>ffmpeg -i input1 -i input2 -c:v copy -c:a copy -map 0:v:0 -map 1:a:0 out</code>