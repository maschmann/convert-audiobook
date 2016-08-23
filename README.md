# convert-audiobook
Convert multiple mp3 files into audiobooks with chapters and album art.

> Thanks to Benjamin Elbers <elbersb@gmail.com> for providing the initial script and giving permission to re-publish and enhance it :-)

## what does it do?
Sometimes I have a lot of audiobook (chapter) mp3 files I want to hear in a row and sometimes my player crashes. If there's just one large mp3, you're doomed and for the single files ist most of the time ok to handle. But having ONE complete audiobook file with chapters is much more comfortable.
This script takes a bunch of mp3s, merges and converts them to aac, creates a chapter file and finishes with a m4b audiobook.

## installation
CAUTION: Please use the latest versions of the mentioned libraries! Otherwise the converter may crash.

```bash
# since ffmpeg is not included in 14.04 any more
sudo add-apt-repository ppa:mc3man/trusty-media
sudo apt-get update
sudo apt-get install ffmpeg gpac mp3wrap python-pymad python-mutagen python-audioread

# get the latest/last version of mp4v2 - maybe I'll include this in to github, here
wget https://storage.googleapis.com/google-code-archive-downloads/v2/code.google.com/mp4v2/mp4v2-2.0.0.tar.bz2
tar xvjf mp4v2-2.0.0.tar.bz2
cd mp4v2-2.0.0/
sudo ./configure
sudo make
sudo make install
```