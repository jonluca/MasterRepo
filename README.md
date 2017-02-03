# MasterRepo

##Please note - on iOS 10, you might receive error 24: too many files

If you receive this error, I'd recommend selectively going through the list and remove smaller repos or repos you don't need. We're still waiting on a reply from saurik on the issue, and whether it's a new OS limitation or whether it's on Cydia's end. 

This is a collection of the most popular and used sources in Cydia as of 2/2/2017

In December 2016, I migrated the MasterRepo to a package on my repo (http://jonlu.ca/repo). The easiest way to install (and stay up to date) is to install that package.

If you would still like to do it manually, navigate to masterrepoeasyinstall/etc/apt/sources.list.d/MasterRepo.list and grab it from there.

To install, just place MasterRepo.list in /etc/apt/sources.list.d

If you encounter any problems, make sure permissions are set to 0655.

The latest release it is known to work on is Cydia 1.1.27, iOS 9.3.3 - however, this should work on virtually any release of Cydia, from iOS 2 to iOS 10. You may encounter limit errors in older versions of Cydia (which were limited to 2^16, or 65536 indivdual packages). Unless Cydia changes the way it handles sources and list files, this file should not cause any problems.

Any other questions should be directed to /u/JonLuca on reddit, or through email at jdecaro@usc.edu
