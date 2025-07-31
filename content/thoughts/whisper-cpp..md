---
title: whisper-cpp.
date: 2025-07-30T19:00:00
---
my brother and i help with my brother's youtube channel [chocoresh](https://youtube.com/@Chocoresh).
he does the video stuff, lighting, editing and all.
for now, i just do the subtitling.

i used to use kdenlive's speech recognition feature that uses vosk under the hood.
now they have also added support for whisper, but it's the python one.
it needs torch, numba and some stuff like that - i have no idea.
so anyway, it errored out.
it said it required python versions between 3.9-3.13.
but i have 3.13.5.
i mean, bruh.

installed whisper-cpp from chaotic-AUR.
got base.en GGML model from huggingface.

stripped the audio from the video file:
```bash
ffmpeg -i video.mp4 -an audio.mp3
```

ran this command:
```bash
whisper-cli -m ggml-base.en.bin\
	-t 1 --max-context 8 -et 2.8\
	-osrt -f audio.mp3
```

there's now an audio.mp3.srt in the current directory.

base.en was pretty fast for my intel core i3.
and output is so much better than vosk.

well, on second glance, i still have to work on the subtitle.
and i don't blame whisper.cpp.
it's that the model gets confused when two people speak at the same time,
and accents can be hard to interpret, even for humans, so.
but it did a good job.

thank you, whisper-cpp devs.
