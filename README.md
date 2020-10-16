# Scripts

## batch265
A simple shell script for converting a folder of videos to H.265/HEVC using handbrakeCLI.
Inspired by the tutorial and script [from Nick Congleton at LinuxConfig.org](https://linuxconfig.org/how-to-use-ffmpeg-to-convert-multiple-media-files-at-once-on-linux)

Script assumes audio is AAC and passes it through unchanged. Output is an MKV container. Default command uses macOS Video Toolbox for accelerated performance. Can be altered for devices without VT hardware.

### Usage
Call script with these arguments: 
1. Extension of files you want to convert. (ex: mp4)
2. Directory of source files. (Files must be in subdirectory of working directory)
3. (OPT) Output directory name. (Default is "recompressed".)
4. (OPT) Quality setting. (0-51. 0 is lossless. 51 is terrible. 28 by default)

### Example commands: 
`$ batch265 mp4 videos`

This will find all files with the extension "mp4" in the subdirectory "videos" of the working directory and convert them to HEVC/H265 with quality 28 and the filetype MKV, placing the results in a "recompressed" subdirectory of the "videos" directory.

`$ batch265 m4a "vacation" "archive" 20`

This will find all files with the extension "m4a" in the subdirectory "vacation" of the working directory and convert them to HEVC/H265 with quality 20 and the filetype MKV, placing the results in the "archive" subdirectory of the "vacation" directory.
