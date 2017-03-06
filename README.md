# MasterRepo

## About
This is a collection of the most popular and used sources in Cydia as of 3/6/2017

In December 2016, I migrated the MasterRepo to a package on my repo (http://jonlu.ca/repo). The easiest way to install (and stay up to date) is to install that package.


## Installation

### Preferred
- Add http://jonlu.ca/repo/
- Add MasterRepoEasyInstall
- Close and reopen Cydia
- Open Cydia, go to Sources, click Edit, remove http://jonlu.ca/repo/ (It's to prevent errors because it is included in MasterRepo.list)

### Manual

- Navigate to masterrepoeasyinstall/etc/apt/sources.list.d/MasterRepo.list
- Save that file and place it in /etc/apt/sources.list.d/

## Common Problems

If you encounter any problems, make sure permissions are set to 0655.


### Error 24: too many files open

In iOS 10, Apple seemingly changed the maximum number of file handles that iOS can deal with at any time. We still do not have a fix for this, and are not 100% sure why it happens.

If you'd still like to use MasterRepo, I'd recommend you navigate to /etc/apt/sources.list.d and edit MasterRepo.list, removing some of the sources you won't use/care about. Try to get the list down to about 20 repos - at that point, you shouldn't get the error anymore.

### Duplicate source entries (MasterRepo.list:# and cydia.list:#)

This occurs when you have the same repo included in the MasterRepo as well as installed manually.

The easiest way to fix this is to remove any repos you've added manually that are included in the MasterRepo. 

There are a couple ways of doing it - sources installed through MasterRepo aren't manually removable, so you can look at masterrepoeasyinstall/etc/apt/sources.list.d/MasterRepo.list and compare it to whats removable on your Sources list.

The other is a bit longer:

1. Look at the errors and copy all the line numbers with errors next to ***cydia.list***. It should look like this:

<img src="http://i.imgur.com/B97ffgH.png" />

2. In the example above there was only one error (only line number 8 next to cydia.list) - you might have more than one, remember them.

3. Navigate to /etc/apt/sources.list.d and open cydia.list (use your favorite file browser, preferably iFile or Filza)

4. Find the line numbers that match the errors above. For the example above, you'd look at line 8. Note: don't edit cydia.list as it's automatically generated and changes to it won't persist.

5. Go back to Cydia, go to Sources, click edit, and remove the sources matching those line numbers. These errors occur because there are duplicate source entries - removing the repo this way won't remove it from your device. It'll still be in MasterRepo.

6. Refresh your repos. If the error persists, double check that you removed all the repos the errors point to.

## Other notes

Any other questions should be directed to /u/JonLuca on reddit, or through email at jdecaro@usc.edu
