# mac-quick-ffmpeg
Mac Quick Action Video Compression

This is a quick action setup using Automator for Mac
It will allow you to right click a movie file and run tight compression on it.

I have seen it optimize a Final Cut Video from 213MB to just 21MB
MOV, etc may vary

Mac only: Sorry Windoz users :) 

So you just got done taking a video with OBS and it's something like 2 min long and 2.8GB in size.. you want to upload it to the Forum but it's just too dang big.  Well if your on a mac, can copy and paste, I have you covered.

First and foremost, OBS does a great job, as does quick time and others for captureing good clean video.. But it's not great at running H264 codecs and doing with tools like FFMPEG can do.  

FFMPEG / FFPROBE - If you do not have these downloaded and installed I'd suggest doing that before this next step.  For the fastest option and one that will work directly with my script.  Install Homebrew on your mac.

https://docs.brew.sh/Installation

After that, inside the open terminal window type: 

Brew install ffmpeg ffprobe
Automator: Next start up automator (Command + Spacebar) type Automator, hit enter

New Quick Action
Workflow Receives : Movie files (in) Finder
Add from the left side : Get selected finder Items (no configs)
Add from the left side: Run Shell Script (Shell /bin/zsh) (pass input: as arguments)

Download this script - Open it and paste into the Shell Script Window

Save : Give it a name

Open Finder and select a video -> Right click it -> Quick action -> your saved name here

This will then prompt for trim at the front, trim at the back, and ask you to select a folder and give the file a name.

One running, you will see a gear icon spinning on your task bar top of the screen, that is your status indicator.  Once done your video should be baked.

Enjoy!
