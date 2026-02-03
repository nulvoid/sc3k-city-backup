# sc3k-city-backup
Don't rely on Steam Cloud to save your cities in Simcity 3000 Unlimited on Steam. If you build full large cities, you will run out of available cloud storage before you finish the second city. Back them up yourself so you never lose them.

## Requirements
-Python 3.6+

-Simcity 3000

-A safe location to backup you cities

Ensure which version of Python you are running with:

`python3 --version`

or

`python --version`

## Using the script
Acquire the script from whatever means you best see fit. In order for the script to work, you will need to change the file paths for "source" and "destin". Once you have properly assigned the file paths, run the script with `python3 sc3kb.py` or `python sc3kb.py`. You will be presented with the options of backing up cities, restoring cities from backup, or exiting. By default, all cities that are included with a base Simcity 3000 Unlimited install are ignored when backing up your cities. This can be changed or expanded manually by adjusting the ignore list.

### source
This is the location of the "Cities" folder in your Simcity 3000 install. If you have Simcity 3000 Unlimited on Steam and are using some form of Linux, changing user to your username should be the correct path. Verify by right clicking the game in your library, hovering over manage, and clicking browse local files. Otherwise, provide the filepath to your Cities folder.

### destin
This is the destination folder for your backed up cities. I have a NAS where I backup my cities to, which is why I made this script in the first place.
