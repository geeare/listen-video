## Listen Visualization

Welcome to the visualization for my new single, Listen! If you saw the YouTube 
video, you may be curious how it was produced. Actually, the entire 
visualization is a python script which is provided here so that you can run the 
exact visualization that I used to create the video!

If you haven't seen the video, be sure and check that out too! https://youtu.be/qX9AyfQ0l7Q


### Running the visualization animation

Ensure that all of the enclosed files are present in the same directory. Then 
open two terminal windows. From the second command line or terminal navigate to 
this folder and run the enclosed `release` program. For the best effect, run it 
from within Swordfish90/cool-retro-term for the cool retro effects. It should 
run just fine, however, in any terminal emulator or command line app you have 
available. You can also set the prompt in the first terminal to an empty prompt
to remove any existing prompt by setting `PS1=""`. This will only take effect 
until you close your terminal, and only in that one.

Note that you may need to adjust the value of the `TTY` variable depending on 
how your OS names TTY devices. If you need a reference, you can run the `tty`
command from the first terminal.

Note that audio playback has been disabled in this preview, but you can always
check out the [YouTube video](https://youtu.be/qX9AyfQ0l7Q) to listen to the 
song again.

The visualization animation has been stripped of any system-dependencies, so it 
should run fine wherever Python 3 is available. Python 3.10 is recommended. 


### Technical Details

The actual animations are implemented as two separate files from the main 
script, `init.txt` and `ascii-vis.c`. The first phase of the animation
where it "initializes" the system and loads the program is covered in the 
init.txt file. Note that `!` characters are not printed; instead these are 
converted into a 10ms pause. You can modify the length of the pauses by adding 
or removing `!`'s as you see fit. You can also modify the text to make it say 
different things.

The second phase, where it prints the logo and C program is stored in 
`ascii-vis.c`, and the timings are more fixed there. Spaces are 
ignored from the timing to help it print "faster" without speeding up the 
animation too much. Each non-space character is printed with a 5ms delay. You 
can modify this file as well, but keep in mind that in its current form it is 
also a fully-valid C program and can be compiled and run like a regular program. 
When run, it will print out "Hello World!" and exit with status 0.

There are two additional "hard-coded" animations in the program; both of which 
are simply implemented using strings as iterators. After running each of these 
it will wait for 5 seconds before clearing the screen and proceeding to the next 
phase. After the last phase, the screen will clear and it will wait for 20 
seconds before exiting. 


### Legal details

Please see the included [LICENSE](https://github.com/geeare/listen-video/blob/main/LICENSE)
file for information about file availability, modifications, and licensing. In 
general, files containing GeeAre artwork are available for redistribution under 
the Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International 
(CC BY-NC-ND 4.0) license. All other files are in the public domain.

![CC BY-NC-ND 4.0](https://i.creativecommons.org/l/by-nc-nd/4.0/88x31.png)
![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png)