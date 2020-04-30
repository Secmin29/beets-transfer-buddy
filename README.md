# Beets Music Transfer Buddy

## Inspiration

I love lossless formats for music, as a properly encoded file should be all but identical to what is present on a CD. While I leave the debate over the ability to discern a difference between FLAC and a 320 or v0 encoded MP3 to others, I am of the opinion that being able to reproduce the original source CD is the greatest benefit (especially after loosing the original source CD).

[Beets](https://beets.io) is an awesome tool that helps organize and tag my music, but at the same time it maintains data about each song is a central database. When setting it up, I discovered the `convert` plugin, and knew that it would be a very simple way to easily convert my lossless music to mp3 before transferring it to my phone. Even better, the plugin will also detect if the music is already in a lossy format (such as music purchased through iTunes), and simply copy the files to the destination.

While reading about beets, I stumbled on [this blog post](https://blog.thomastoye.be/how-i-manage-my-music-on-linux-56c09ad43a00), which documented using rsync to transfer the converted music directly to a phone using SSH. After running this manually a few times, I wanted to wrap the whole process into a script. This is the result.

## Requirements

* Beets (obviously)
* Ability to run an SSH server on your phone. I use [SSHelper](https://arachnoid.com/android/SSHelper/index.html), but anything else should work

## Installation

* Place script in your $PATH

## Usage

```
Beets Music Transfer Buddy:
Transfer music to phone via SSH. Will convert to lossy codec, or directly copy if already in lossy format.

Options:
--artist=ARTIST   Artist to convert and transfer to phone
--album=ALBUM     Album to convert and transfer to phone
```