# battle-video-archive
This is a repository of some of the battle videos uploaded as part of Smogon's [Battle Maison](https://www.smogon.com/forums/threads/battle-maison-discussion-records.3492706/) and [Battle Tree](https://www.smogon.com/forums/threads/battle-tree-discussion-and-records.3587215/) streak submissions following the shutdown of the 3DS servers. These are the raw battle video files, only usable by the game.

The battle videos have been sorted into folders for each streak. Additionally, each streak includes a text file describing the teams used and some basic information about each video.

## How To Use
In the time between videos starting to get downloaded and this repo's initialization, Citra has been killed and some forks or new offshoots have come up.
Since this event is fresh and the 3DS emulator scene has yet to settle or produce a frontrunner, these playback instructions will be written for Citra.

Any future emulator frontrunners are likely to be either be a fork of Citra, or have a similar interface to Citra's, so these instructions should still apply or can be easily adapted.

### Pre-requisites
Most videos will NOT play without taking steps to ensure battle video compatability.
1. Use the later games in each gen (Omega Ruby, Alpha Sapphire, Ultra Sun, or Ultra Moon) for viewing battle videos.
2. Install the game's updates. From Citra's File menu, select "Install CIA..." and select the latest update in CIA format for the game. For ORAS this is v1.4, and for USUM this is v1.2.

ORAS v1.4 can natively play all XYORAS battle videos regardless of game or update version.

USUM v1.2 will not play battle videos that are not USUM v1.2. However, all gen 7 battle videos in this repo have been changed to read as USUM v1.2 videos. This might mean that some of the changed battle videos will desync when played back, but testing shows that this seems to not be an issue. The original battle videos are available for download in the releases section to the right of this repo's main page.

### Citra Directions
1. Download any number of battle videos to a location on your computer. Individual videos can be downloaded on GitHub by selecting/opening a video file, then using the download button found on the upper right.
2. The downloaded videos will need to be copied to the game's extdata folder.
   - The easiest way to find the extdata folder is by right-clicking the game from Citra's game menu and selecting "Open Extra Data Location".
      Alternatively, select File then "Open Citra Folder". From your Citra folder, descend to `sdmc\Nintendo 3DS\00000000000000000000000000000000\00000000000000000000000000000000\extdata\00000000\<titleid>`, where `<titleid>` is the titleid of the particular game *. For example, `00001B50` is Ultra Sun's titleid. The titleid of each game can be Googled.
     - \* This path will not exist if the game has not been started previously.
   - Descend to `user\btvideo`.
   - Copy the battle videos to the `btvideo` folder.
   - Rename the battle videos. They must be named with 3 numeric digits, and can only be in the range `000-099`, and cannot have a file extension. They must include leading zeroes to be 3 digits long. For example, `042` is a valid battle video filename, and `42.bin` is not.
3. Launch the game and use the Vs. Recorder to view the battle videos. Having a save file that has progressed past the introduction and has obtained the Vs. Recorder is highly recommended.
