#Save web cam output files to dropbox

December 23, 2012

dropbox, linux, motion, symlinks, ubuntu, web cam

I use the [motion web cam daemon](http://www.lavrsen.dk/foswiki/bin/view/Motion/WebHome), running on Ubuntu, to save files to Dropbox. I did not want to configure motion to save files inside my home directory where my Dropbox folder is located; the daemon is run by the motion user which can’t write to my home directory in any case. It turns out Dropbox will work with symlinks.

This was the command I used (run from the DropBox directory):

    ln -s /tmp/motion/ ./motion

More details [here](http://lifehacker.com/5154698/sync-files-and-folders-outside-your-my-dropbox-folder)

