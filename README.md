# wavmarkers: Split an audio file on markers


## Introduction

Some audio formats support "markers" or "chapters" or "cues".

This program uses `ffmpeg` to split an audio file into separate files using
these markers.

Requires Ruby and a modern `ffmpeg` to be installed.

## Gapless reconstruction

Note: Some formats do not perfectly round-trip without gaps.  WAV, AIFF and OGG
and M4A can be split and later concatenated (via something like `sox`) with no
clips in the audio.  To the best my knowledge, MP3 cannot, because it works in
a multiple of a fixed number of samples.
