# WEDI - File Editing and Tracking Utility

## Overview
**WEDI** is a shell script utility designed to assist users in editing files within a directory while keeping track of editing activities. It provides functionalities for opening, listing, and tracking edits to files, enhancing the user's productivity and organization when working with multiple files.

## Features
- **File Editing**: WEDI allows users to edit files within a specified directory using their preferred text editor.
- **File Tracking**: The utility maintains a log of editing activities, recording details such as file names, directories, timestamps, and editing frequencies.
- **File Listing**: Users can list files that have been edited within a directory, optionally filtering the list based on specific dates.

## Requirements
- Unix-like operating system (Linux, FreeBSD)
- Shell environment (Bash)
- Standard POSIX utilities (`date`, `sed`)
- Optional utilities (`gdate`, `gsed`, `realpath`)

## Installation
1. Download the WEDI script file to your system.
2. Ensure the script has executable permissions (`chmod +x wedi.sh`).
3. Optionally, customize environment variables and settings within the script.

## Usage
```sh
./wedi.sh [OPTIONS] [ARGUMENTS]
```

### Options
- `-m`: Edit the file that has been edited the most within the directory.
- `-l`: List files edited within the directory.
- `-a DATE`: List files edited after the specified date.
- `-b DATE`: List files edited before the specified date.

### Arguments
- `[DIRECTORY]`: Specify the directory in which to perform editing or listing operations.
- `[FILE]`: Specify the file to edit within the directory.

## Examples
1. Edit a file within the current directory:
    ```sh
    ./wedi.sh example.txt
    ```

2. Edit a file within a specific directory:
    ```sh
    ./wedi.sh /path/to/directory/example.txt
    ```

3. List all edited files within the current directory:
    ```sh
    ./wedi.sh -l
    ```

4. List files edited after a specific date:
    ```sh
    ./wedi.sh -a 2024-01-01
    ```

5. Edit the most frequently edited file within the directory:
    ```sh
    ./wedi.sh -m
    ```
