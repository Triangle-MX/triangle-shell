# Triangle-Shell
A super-powered shell script to help us with our development process. Keep in mind that this shell script was decided to be used on the <a href="https://github.com/Triangle-MX/Triangle-4.0">Triangle-4.0 Site</a>.

## Why?
At Triangle we have always hated typing each ```sass```, ```browser-sync```, ```ruby``` commands completely, that is why we decided to write **our own** shell script to increase our performance.

## How is it built?
Everything is compiled in a **single command** (```triangle-site```), but this command has several routines (for example: ```triangle-site sass```).

## Functionality
How our super-powered shell script works:

### Routines
The command's functions are divided into routines. This are the current routines you can run with the ```triangle-site```command:
- ```sass```: Starts watching a ```.sass``` document (in our case, ```main.sass```).
- ```browser-sync```: Starts running a live-development preview with ```browser-sync```.
- ```dev```: Opens your preffered code editor (in our case <a href="https://atom.io">Github's Atom</a>).
- ```view-site```: Opens our site.
- ```docs```: Opens the Docs.

### How are routines built?
If you go inside the ```triangle-site``` file, you will see each routine is built like this:
``` shell
# If Statement, controlling that the 1st varible is equal to the routine name:
if [ "$1" = "browser-sync" ]
then
    # Makes shure it is in the desired directory:
    cd
    cd Desktop/Triangle/A-Site-4.0/
    
    # Explains what it's going to do:
    echo Triangle Site 4.0: Running with Browser-Sync
    say Triangle Site 4.0: Running with Browser-Sync
    
    # Does it:
    browser-sync start --server --files "css/*.css, *.html, */*.html js/*.js js/vendor/*.js"
fi
```
So adding routines is pretty damn easy.

## How can I use it?
It's simple, just download it (the shell script file) and get it to ```/usr/local/bin```. Then, change the permissions so you can execute it without using ```sudo```.

Once you have done this, go to your command line and type ```triangle-site routine-name``` to run certain routine.

Notice the shell script is only available for **macOS users**.
