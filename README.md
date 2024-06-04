# battle-video-archive
This is a repository of some of the battle videos uploaded as part of Smogon's [Battle Maison](https://www.smogon.com/forums/threads/battle-maison-discussion-records.3492706/) and [Battle Tree](https://www.smogon.com/forums/threads/battle-tree-discussion-and-records.3587215/) streak submissions following the shutdown of the 3DS servers. These are the raw battle video files, only usable by the game.

The battle videos have been sorted into folders for each streak. Additionally, each streak includes a text file describing the teams used and some basic information about each video.

## How To Use
The files can be navigated by entering the XY_ORAS or SM_USUM folders above, and then descending into the format, username, and streak folders listed under the games folder. Alternatively, all of the battle videos can be downloaded by selecting the Battle Video Download link to the right on this GitHub repo's main page.

Jump to "Homebrew 3DS Instructions" if NOT planning to use the battle videos with Citra.

In the time between videos starting to get downloaded and this repo's initialization, Citra has been killed and some forks or new offshoots have come up.
Since this event is fresh and the 3DS emulator scene has yet to settle or produce a frontrunner, these playback instructions will be written for Citra.

Any future emulator frontrunners are likely to be either be a fork of Citra, or have a similar interface to Citra's, so these instructions should still apply or can be easily adapted.

### Pre-requisites
Most videos will NOT play without taking steps to ensure battle video compatability.
1. Use the later games in each gen (Omega Ruby, Alpha Sapphire, Ultra Sun, or Ultra Moon) for viewing battle videos.
2. Install the game's updates. From Citra's File menu, select "Install CIA..." and select the latest update in CIA format for the game. For ORAS this is v1.4, and for USUM this is v1.2.

ORAS v1.4 can natively play all XYORAS battle videos regardless of game or update version.

USUM v1.2 will not play battle videos that are not USUM v1.2. However, all gen 7 battle videos in this repo have been changed to read as USUM v1.2 videos. This means that some of the changed battle videos might desync when played back, but desyncs did not occur during testing. Please notify me if there are any issues with this. The unedited battle videos are available for download in the releases section to the right of this repo's main page.

### Citra Instructions
1. Download any number of battle videos to a location on your computer. Individual videos can be downloaded on GitHub by selecting/opening a video file, then using the download button found on the upper right.
2. The downloaded videos will need to be copied to the game's extdata folder.
   - The easiest way to find the extdata folder is by right-clicking the game from Citra's game menu and selecting "Open Extra Data Location".

     Alternatively, select File then "Open Citra Folder". From your Citra folder, descend to `sdmc\Nintendo 3DS\00000000000000000000000000000000\00000000000000000000000000000000\extdata\00000000\<titleid>`, where `<titleid>` is the titleid of the particular game *. For example, `00001B50` is Ultra Sun's titleid. The titleid of each game can be Googled.
     - \* This path will not exist if the game has never been launched.
   - Descend to `user\btvideo`.
   - Copy the battle videos to the `btvideo` folder. Do not copy or create a new folder in `btvideo`.
3. Rename the battle videos. They must be named with 3 numeric digits, and can only be in the range `000-099`, and cannot have a file extension. They must include leading zeroes to be 3 digits long. For example, `042` is a valid battle video filename, and `42.bin` is not.
4. Launch the game and use the Vs. Recorder to view the battle videos. Having a save file that has progressed past the introduction and has obtained the Vs. Recorder is highly recommended.

### Homebrew 3DS Instructions
1. Follow the "Dumping Instructions" below.
2. Viewing the SD card on a PC, navigate to `3ds\Checkpoint\extdata\<game ID and name>`. The folder named within Checkpoint should be visible.
3. Copy the folder to the same location. By default on Windows, the new folder will be named with an appended ` - Copy`. This is fine to keep.
My personal convention is to keep the same folder name but instead append `edit`. So for example, my `3ds\Checkpoint\extdata\<game ID and name>` folder should contain two folders: `20240408-0102` and `20240408-0102edit`
Keeping the same name but appending the `edit` is useful to reference later. The folder without the edit was the state of the battle videos before dumping without any changes, and the `edit` folder contains changes.
4. Enter the copied extdata folder, then enter `btvideo`. The full path is `3ds\Checkpoint\extdata\<game ID and name>\<copied folder>\btvideo`.
5. Copy battle videos into this folder. Do not copy or create a new folder in `btvideo`.
6. Rename the battle videos. They must be named with 3 numeric digits, and can only be in the range `000-099`, and cannot have a file extension. They must include leading zeroes to be 3 digits long. For example, `042` is a valid battle video filename, and `42.bin` is not.
7. Insert the SD card into the 3DS and launch Checkpoint.
8. If any game cart is inserted in the system, wait for it to appear as a tile.
9. Press `X` to change to extdata mode.
10. From the top screen, select the title and press `A`. The "New..." option should now be flashing in blue on the lower screen.
11. From the bottom screen, select the copied folder containing the downloaded battle videos. Press `R` to set this extdata as the current extdata for the title, and `A` to confirm.
   - Note that the untouched folder that was originally dumped into can also be restored from. This will undo any changes made by restoring the copied extdata.
12. Once Checkpoint is finished writing, it can be closed.
13. Launch the game and use the Vs. Recorder to view the battle videos.

## Dumping Battle Videos
Battle videos can only be dumped from 3DS systems with homebrew.

Note that battle videos are stored to the console, and are not stored on the cartridge. So it is NOT possible to take the game cart and use it with any homebrew 3DS to dump battle videos.

A 3DS with battle videos can be homebrewed at any time; the console did not have to be homebrewed at the time the battle video was saved in order to dump it.

### Dumping Instructions
These instructions are written for the Checkpoint save manager 3DS homebrew app. This app is part of the stock homebrew installation. This process should be possible with other 3DS save managers.
1. Launch Checkpoint on the 3DS.
2. If any game cart is inserted in the system, wait for it to appear as a tile.
3. Press `X` to change to extdata mode.
4. From the top screen, select the title to dump from and press `A`. The "New..." option should now be flashing in blue on the lower screen.
5. Press `A` to dump to a new folder. Press `A` again to confirm.
6. Choose a folder name, then confirm. The default name option as the current date+time is recommended, as it can be a helpful reference.
7. After the extdata dumps, Checkpoint can be closed. The system can be shut down as well, unless FTP is planned to be used to transfer the files to PC.
8. The battle videos can be found on the system's SD card from the root at: `3ds\Checkpoint\extdata\<game ID and name>\<named folder>\btvideo`. These files are the battle videos.
