#Removing orphaned packages on Ubuntu

August 22, 2013

orphaned, packages, ubuntu

The deborphan tool finds packages that have no packages depending on them. The default operation is to search only within the libs and oldlibs sections to hunt down unused libraries.

``sudo apt-get install deborphan``

``sudo deborphan | xargs sudo apt-get -y remove --purge```