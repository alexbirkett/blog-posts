Don’t fork with another guys coding conventions

June 13, 2012

Various bosses drilled into me the importance of coding conventions during many years developing Symbian OS software. The Symbian coding conventions, described a decade ago as ‘revolutionary’, were idiosyncratic. Braces were indented using the whitesmiths style. Functions that threw Symbian’s equivalent of an exception, a ‘leave’, had to end with the letter L. Other functions that could ‘leave’ and add object to what was known as the cleanup stack ended with the letters LC. The int type was typeddefed to TInt. Use of int was forbidden because in the future, Symbian may choose to redefine TInt as something other than a 32 bit signed value! (As far as I’m aware, Symbian slipped into obsolescence before this ever happened – and let’s face it was unlikely to ever occur) In the Symbian world, the coding conventions were clearly defined and not following them was a sign of incompetence.

When starting developing for Android I learned that Google prefixed their member variables with the letter m and assumed this was a common convention for all Android apps. I’m also a fan of long, descriptive variable names and short methods.

At the end of last year I forked the [CWAC Location Poller project](https://github.com/alexbirkett/cwac-locpoll) on github. It was almost what I needed for my [Android Phonelocator app](https://github.com/alexbirkett/phonelocator-android). It just needed a few more features. When I saw the code I refactored with abandon. The Android m variable name convention was not used, variable names were abbreviated and I felt that some of the methods needed to be split up into smaller methods. I assumed that the original author of the work would be delighted that somebody who new what they were doing had fixed their code for them.

After  submitting the pull request I discovered that the creator of the code was [‘commons ware guy’ Mark Murphy](https://twitter.com/#!/commonsguy). Author of several [Android books](http://commonsware.com/), [top ranking Android user on stackoverflow](http://stackoverflow.com/tags/android/topusers) and general Android key person of influence. Mark politely rejected my pull request and was kind enough to link to my fork from his.

Mark has since fixed some bugs on his orignal fork. Due to my refactoring, it was not viable to automatically merge his changes into my fork. So I had to manually merging the changes over. I’ve been left maintaing a project I just wanted to add a feature to simply because I messed with Mark’s coding conventions.

This experience has taught me a lesson. If you want your feature accepted into a project. Just change what is necessary, don’t meddle with other things unrelated to your change, like coding conventions!

‹ Eniro GuleSider app for AndroidBuilding a GPS tracking web site platform – Creative breakfast @MESHNorway ›
Tagged with: Android, clean code, coding conventions, commonsguy, fork, MESHNorway, Phonelocator