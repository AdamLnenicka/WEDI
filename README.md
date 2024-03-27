### Introduction
The Wedi Shell Script is a utility designed to manage and edit files within a specified directory. It provides functionality to track file edits, list edited files, and edit files using a chosen text editor.
Offers a convenient way to manage and track file edits within a specified directory. With its flexible options, it provides useful functionality for both casual users and system administrators.

### Usage
To use the Wedi Shell Script, follow the instructions below:

#### Setting Up Environment
1. Ensure that the script has executable permissions.
2. Place the script in a directory accessible in your system's PATH.

#### Running the Script
```sh
./wedi.sh [OPTIONS] [DIRECTORY] [DATE]
```

#### Options
- `-m`: Edit the file that has been edited the most in the specified directory.
- `-l`: List all files edited within the specified directory.
- `-a DATE`: List files edited after the specified date within the specified directory.
- `-b DATE`: List files edited before the specified date within the specified directory.

#### Arguments
- `DIRECTORY`: (Optional) The directory in which to operate. If not provided, the current directory is used.
- `DATE`: (Optional) A date in the format "YYYY-MM-DD" to filter file edits.

### Functionality
The Wedi Shell Script provides the following functionality:

#### File Editing
- Edit a specified file using the default or specified text editor.
- Track the number of times a file has been edited and record the timestamp of each edit.

#### File Listing
- List all files edited within a specified directory.
- List files edited after or before a specified date within a specified directory.

#### Error Handling
- The script handles various error conditions, such as invalid arguments, missing utilities, and permissions issues.

### Dependencies
- The script utilizes standard Unix utilities like `date`, `sed`, and `realpath`.
- On FreeBSD systems, it requires `gdate` and `gsed` for extended functionality.

### Notes
- Ensure that the specified text editor (set in `EDITOR` or `VISUAL` environment variables) is installed and accessible.
- The script maintains a record of edited files in a designated file specified by the `WEDI_RC` environment variable.

### Example Usage
1. Edit the most frequently edited file in the current directory:
   ```sh
   ./wedi.sh -m
   ```

2. List all edited files in a specific directory:
   ```sh
   ./wedi.sh -l /path/to/directory
   ```

3. List files edited after a certain date in a specific directory:
   ```sh
   ./wedi.sh -a 2023-01-01 /path/to/directory
   ```

4. Edit a specific file in a specific directory:
   ```sh
   ./wedi.sh /path/to/directory/filename.txt
   ```
