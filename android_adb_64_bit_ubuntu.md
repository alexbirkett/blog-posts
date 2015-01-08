#Why does the Android adb not run on my 64 bit Ubuntu installation?

January 8, 2013

You need to install the ia32-libraries like this:

    sudo apt-get install ia32-libs