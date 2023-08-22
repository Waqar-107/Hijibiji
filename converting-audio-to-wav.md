I had a recording in the format `m4a` which I needed to convert into `ffmpeg` format. This can actually convert different formats of files. 
In order to do that, we first need to install a package on Ubuntu using `sudo apt-get install ffmpeg`. 
We can check the version of the installed package using `ffmpeg -version`.

Assuming we have an mp3 file, we use the command,
`ffmpeg -i infile.mp3  -ar 16000 -ac 1  outfile.wav`. Note that here `16000` is a frequency that is often required by speech to text converter like Mozilla deepspeech
