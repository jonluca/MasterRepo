# MasterRepo

## About
This is a collection of the most popular and used sources in Cydia as of 3/6/2017

In December 2016, I migrated the MasterRepo to a package on my repo (http://jonlu.ca/repo). The easiest way to install (and stay up to date) is to install that package.


## Installation

### Preferred
- Add http://jonlu.ca/repo/
- Add MasterRepoEasyInstall
- Close and reopen Cydia
- Open Cydia, go to Sources, click Edit, remove http://jonlu.ca/repo/ (Don't worry, it's to prevent errors because it is included in MasterRepo.list)

### Manual

- Navigate to masterrepoeasyinstall/etc/apt/sources.list.d/MasterRepo.list
- Save that file and place it in /etc/apt/sources.list.d/

## Common Problems

If you encounter any problems, make sure permissions are set to 0655.


### Error 24: too many files open

If you receive this error, I'd recommend selectively going through the list and remove smaller repos or repos you don't need. We're still waiting on a reply from saurik on the issue, and whether it's a new OS limitation or whether it's on Cydia's end. 

### Duplicate source entries (MasterRepo.list:# and cydia.list:#)

This occurs when you have the same repo included in the MasterRepo as well as installed manually.

The easiest way to fix this is to remove any repos you've added manually that are included in the MasterRepo. 

There are a couple ways of doing it - sources installed through MasterRepo aren't manually removable, so you can look at masterrepoeasyinstall/etc/apt/sources.list.d/MasterRepo.list and compare it to whats removable on your Sources list.

The other is a bit longer:

1. Look at the errors and copy all the line numbers with errors next to ***cydia.list***. It should look like this:

<img src="http://i.imgur.com/B97ffgH.png" />

Any other questions should be directed to /u/JonLuca on reddit, or through email at jdecaro@usc.edu
