## What is Linux?

1. Linux is an open-source operating system kernel created by Linus Torvalds in 1991. It's the core component of various Linux distributions used on servers, desktops, and other devices. Linux is known for its stability, security, and versatility, with popular distributions like Ubuntu and Fedora offering user-friendly interfaces and software packages.

### Listing commands

`ls option_flag arguments `-->It will show the full list or content of your directory.

Examples:

- `ls -l`--> displays detailed information about files and directories..
- `ls -a `--> Represent all files Include hidden files and directories in the listing.
- `ls -i ` --> displays the index number (inode) of each file and directory.
- ` ls -S` --> Sort files and directories by their sizes, listing the largest ones first.

### Directoy commands

- `pwd` --> Present working directory.

- `cd path_to_directory` --> change directory to the provided path.

- `cd ~ ` or just `cd ` --> change directory to the home directory.

- `cd -` --> Go to the last working directory.

- ` cd ..` --> change directory to one step back.

- ` cd ../..` --> Change directory to 2 levels back.

- `mkdir` --> allows the user to create directories

Examples:

```
mkdir xyz                      # make a new folder 'xyz'

mkdir .xyz                     # make a hidden directory

mkdir A B C D                  # make multiple directories at the same time

mkdir -p  A/B/C/D              # make a nested directory

```
