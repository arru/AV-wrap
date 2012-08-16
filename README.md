AV-wrap
=======

Bash script for importing AVCHD movies into m4v/mov with the aid of ffmpeg.
This initial version will re-wrap AVCHD content in full off a mounted memory card and place the output in iPhoto's Auto import folder (OSX-specific). The resulting mp4 video files will then be imported the next time iPhoto is run, or if it is already running, at qutting time. The modification dates of movie files are preserved after re-wrapping.

Imported movie files are renamed as such:
AVCHD-YYMMDD-NNNNNN
which includes the modification date along with the original AVCHD file name (NNNNNN). Example:
AVCHD-20120819-122050.m4v

Requirements: FFMPEG installed and compiled with AAC encoding support.
Camera movies must be recorded to AVCHD, with:
* an mp4-compatible video codec: h.263,h.264,MPEG4. Video will be re-wrapped without altering original data.
* any audio codec intelligible to FFMPEG. Audio will be transcoded to 192k AAC

Future versions will allow configuring how audio and video is handled, as well as where the output is directed. An option will also be added to delete original AVCHD files if importing was successful.