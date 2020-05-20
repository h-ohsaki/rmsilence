# NAME

rmsilence - remove silent parts from specified video files

# DESCRIPTION

**rmsilence** is a Perl script for automatically removing silent parts (video
segemnts with silent audio tracks) from video files.  For every video file
specifed as command-line arguments, **rmsilence** uses the **silentdetect**
audio filter in FFmpeg for detecting silent parts in a video file.  Non-silent
parts are extracted from the original video files, and those files are
concatenated as a single video file.  All video files without silent parts are
stored in the output directoary (/tmp by default).  You can specify the output
directoary with -d option.

# REQUIREMENTS

- Perl verison 5.0 or later
- FFmpeg (https://ffmpeg.org/)

# EXAMPLE

```sh
mkdir out
rmsilence -d out *.flv
```

# INSTALLATION

Simlpy copy the script **rmsilence** to any directoary in your search path.
An example session on UNIX systems:

```sh
wget https://raw.githubusercontent.com/h-ohsaki/rmsilence/master/rmsilence
sudo install rmsilence /usr/local/bin
```

# AVAILABILITY

The latest version of **rmsilence** is available at https://github.com/h-ohsaki/rmsilence .

# AUTHOR

Hiroyuki Ohsaki (ohsaki[atmark]lsnl.jp)
