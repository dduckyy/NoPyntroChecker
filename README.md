# NoPyntroChecker
A small python script used for verifying the contents of a game file using the No-Intro database.

## Why is this needed?
No-Intro's testimony explains it pretty well [here](https://no-intro.org/).

**TL;DR:** Preservation is important, and it is very common to see ROM dumps that are tampered with for various reasons. This script makes checking your ROM dumps easy and encourages people to search for those "original/unmodified dumps".
## How does it work?
Once you run the script, it does the following below:
1. Downloads the No-Intro database to a local folder.
2. Generates an MD5 hash from the file you selected.
3. Searches No-Intro's database for your hash.
4. Returns results based on analysis.
## Requirements
Python 3+, an active internet connection, and your choice of game files. That's it! Make sure your console is supported by looking at the list of No-Intro's supported platforms on the dropdown on [their website](https://datomatic.no-intro.org/). (shown below)
![](https://raw.githubusercontent.com/dvcky/NoPyntroChecker/master/supported-platforms.png)

## Usage
Pretty simple, just download the NoPyntroChecker repository [here](https://github.com/dvcky/NoPyntroChecker/archive/master.zip) and extract the "nopyntrochecker.py" file from the repository's zip file to your preferred location. As long as you have Python installed, you should be able to run it from your terminal. Usage below: 
```
py nopyntrochecker.py /path/to/file/filename.filetype
```
This script is now also compatible with folders, shown here:
```
py nopyntrochecker.py /path/to/folder/
```
Using a folder as the argument will scan every file in it, along with logging a the check into an additional file. This feature will be added to single files eventually as well, although cleaning up the code and fixing a few bugs is the primary focus at the moment.

## FAQ
#### "I have a ROM that runs on my console/emulator fine with no issues, and your script said no matches!"
That is most likely the releaser's intent. Groups that release ROM dumps often look for less noticable things they can take out of/add to ROMs, whether that be to conserve space or "enhance the user's experience" in some form. **CLARIFICATION: This program is _NOT_ meant for verifying that your ROM is "working" or "real", but rather that it is the original/unmodified dump.**
#### "I am confident that my ROM is unmodified, but your script still said no matches!"
Aw shucks. Most likely No-Intro's database API has changed or been updated. The site has stayed pretty consistent on how it functioned for years, but this is bound to potentially happen at one point or another. If it does happen, it will make the script completely unusable until updated. This is sadly not something I can avoid.
