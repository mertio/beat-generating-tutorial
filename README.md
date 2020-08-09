# Beat Generating Tutorial

This is a tutorial for generating beats from your own songs for the SideQuest game "Hit The Stars Unlimited". It is public and free for anyone to use. 
<br><br>
You should get an "output" file that has folders with the names of your songs and in these folders should be files such as:
<br><br>
-> songname (folder)
<br>
---> songname.mp3
<br>
---> drums_easy.txt
<br>
---> drums_medium.txt
<br>
---> drums_hard.txt
<br>

## System Requirements

- A computer that has at least 8 GB of RAM.
- 2 GB of hard disk space

### Preparing The Music

Before starting, let's prepare the music we want to convert.

1) Create a folder and put the songs you want into it. I suggest only a few for your first try since it can take a long time.
2) They should all be mp3 files.
3) IMPORTANT: They should only contain English characters and not other alphabets like : ç, ü, ğ, ö, etc.
4) Name all your songs in a nice format like (band - songname.mp3) since they will be shown in the game that way.
5) I suggest your mp3 files should not exceed 6 MB each for RAM purposes.

### Installing Docker

First we need to install Docker Desktop to our computer:
<br>
https://www.docker.com/products/docker-desktop

### Setting up enough RAM for Docker to use

After installing Docker, we need to assign at least 6 GB of RAM to it. This is because the AI needs a lot of RAM to generate the beats:

![Alt text](dockerSettings.png?raw=true)

### Running the Docker command

After setting up Docker, all we need to do is open the command line and run the command:
```
docker run -ti -v <absolute-path-of-folder-where-all-our-music-is>:/music/ mertbbicak/auto-drum-transcription:1.0.0
```
I advise try first with a small number of songs at first, since it can take a while. After the command is complete, we should get an "output" folder inside our own music folder with each song having its own folder, along with their beat files. The folder structure should look something like this:
<br><br>

-> output
<br>
----> song1
<br>
------> song1.mp3
<br>
------> drums_easy.txt
<br>
------> drums_medium.txt
<br>
------> drums_hard.txt
<br>
----> song2
<br>
------> song2.mp3
<br>
------> drums_easy.txt
<br>
------> drums_medium.txt
<br>
------> drums_hard.txt

### Putting the songs into the game

Now all that's left to do is copy these music folders into our game folder. The directory below is where we will copy them:
```
/Android/data/com.mertbbicak.HitTheStars/files/DrumGame/Tracks/
```
<br>
- Note: We create the DrumGame and Tracks folders ourselves
<br>
So the Tracks folder should contain the music folders like:
<br>
--> Tracks
<br>
----> song1
<br>
----> song2
<br>
----> song3
<br>
<br>
... and so on

### Open up the game and enjoy

If everything is done right, we will see our own songs in the game with star prefixes in front of them. I hope you enjoy!
