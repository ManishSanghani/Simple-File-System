# Simple File System (SFS) Project

This project implements a simple file system (SFS) in C, simulating basic file and directory operations on a virtual disk. The file system is managed through a command-line interface and operates on a disk image file (`sfs.disk`).

## Features
- Directory and file creation
- File content storage (up to 3072 bytes per file)
- Directory navigation (cd, rd)
- File and directory listing (ls)
- File display (display)
- File and empty directory removal (rm)
- Disk and inode usage statistics (stats)

## Files
- `202101201_project1.c`: Main source code implementing the SFS.
- `sfs.disk`: The virtual disk file used by the file system.
- `202101201_project1.exe`: Compiled executable (Windows).

## How to Build

1. Make sure you have a C compiler (e.g., GCC) installed.
2. Compile the source code:
   ```sh
   gcc 202101201_project1.c -o sfs
   ```
3. Ensure `sfs.disk` exists in the same directory. (You may need to create or initialize it as per your assignment instructions.)

## How to Run

Run the executable:
```sh
./sfs
```
On Windows, you can run:
```sh
202101201_project1.exe
```

## Commands
- `ls` — List files and directories in the current directory
- `md <dir>` — Make a new directory
- `cd <dir>` — Change to a directory
- `rd` — Return to the root directory
- `create <file>` — Create a new file (input up to 3072 characters, end with ESC+ENTER)
- `display <file>` — Show the contents of a file
- `rm <name>` — Remove a file or an empty directory
- `stats` — Show free disk blocks and inode entries
- `exit` — Exit the file system
- `help` — Show available commands

## Notes
- Directories can only be removed if they are empty.
- File and directory names are limited to 252 characters.
- Each directory can contain up to 12 entries (3 blocks × 4 entries per block).
- The file system is simulated and does not affect your real disk.

## License
This project is for educational purposes. 