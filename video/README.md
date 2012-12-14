Some ffmpeg commands that I use every so often, but always need to lookup in the (bad) ffmpeg documentation.

Extract frames from a video:
    ffmpeg -i infile.MP4 -r 2 -b:v 24000 -f image2 images/%06d.jpg

Extract frames from a video and also flip the output vertically and horizontally:
    ffmpeg -i infile.MP4 -r 2 -b:v 24000 -vf "vflip,hflip" -f image2 images/%06d.jpg

Assemble the images above into a video file:
    ffmpeg -i images/%6d.jpg -r 30 -b:v 8000k video.mp4

