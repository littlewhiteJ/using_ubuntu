# Alarm when programming
well~

it may be **very convenient** to set an alarm when your long-time programs finished.

i used a system call in python, it is so easy

just
```
  import os
  os.system('paplay mokou.wav')
```

yeah, you may change another music player which is more powerful, but for me, paplay is just ok.

remember that paplay can only play .wav music, so...

i used **ffmpeg**

it can turn a .mp3 music to a .wav music easily~

```
  $ ffmpeg -i mokou.mp3 mokou.wav
```

and when my program is finished, my program will play the music for me!!!
