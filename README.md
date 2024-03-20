## Script to make Hardware Video De/Encoding easier

This script makes Transcoding of Videos using hardware acceleration very easy.
You don't have to deal with all hardware specific parameters.
In the background, The script uses ffmpeg.
It also determines a sufficient codec for the video depending on the video resolution. For Full-HD Videos it will use H.264 and for higher resolutions it will use HEVC. But you can also specify another codec if the defaults are not what you need.

The script will always see if your GPU supports Hardware-De/Encoding and than fall back to the CPU.

Currently, the VA-API acceleartion method works, NVENC might work.

Furthermore, you can set a quality. Higher Values are better. The quality range differs from codec to codec:
- H.264 and HEVC: 0-51
- VP8/VP9 and AV1: 0-63

If you want to force the script to use your CPU, you can set --slow parameter.