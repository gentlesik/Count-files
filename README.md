# Count Files
A little command-line interface (CLI) utility written in Python to help you
count files, grouped by extension, in a directory. By default, it will count
files recursively in current working directory and all of its subdirectories,
and will display a table showing the frequency for each file extension (e.g.:
.txt, .py, .html, .css) and the total number of files found. Any hidden files
or folders (those with names starting with '.') are ignored by default.

![Count-files screenshot](https://user-images.githubusercontent.com/18650184/39443000-1bd83b62-4cab-11e8-9942-242ba29232d7.png)

Optionally, you can pass it a path to the directory to scan. If you prefer, you can leave that argument empty, and it will scan the current working directory.

The optional `-nr` (i.e., "no recursion") switch argument tells the
application not to scan recursively through the subdirectories.

By default, the table will be sorted by the file extension frequency. If you
prefer alphabetically sorted results, you just need to add the `-alpha`
argument.

Similarly, the optional `-nt` (i.e., "no table") switch tells the application
not to show a table listing all the found file extensions and their respective
frequencies, so that it will only display the total number of files.

By default, it will ignore files and directories that are supposed to be
hidden (with names starting with '.', but you can add the `-a` optional
switch argument to make it count all files.



## Examples of usage:

Get a little help about how to use this application:

`countfiles.py -h`
`countfiles.py --help`


Count all files in current working directory and all of its subdirectories, ignoring hidden files and hidden subdirectories:

`countfiles.py`

Count all files in current working directory and all of its subdirectories, including hidden files and hidden subdirectories:

`countfiles.py -a`


Count all files in current working directory, ignoring hidden files and hidden subdirectories, and without recursing through subdirectories:

`countfiles.py -nr`


Count all files in a given directory with recursion:

`countfiles.py ~/Documents`


Count all files in a given directory with recursion, but don't display a table, only the total number of files:

`countfiles.py -nt ~/Documents`


Count all files in a given directory without recursing through subdirectories, and sort the table alphabetically:

`countfiles.py -nr -alpha ~/Documents`

Count all files in a given directory without recursing through subdirectories, including hidden files, and only displaying the total number of files (no table):

`countfiles.py -nr -nt -a ~/Documents`


## Dependencies:

To run this application, you just need to have a working Python 3.6+ instalation. No further dependencies.

The main file should have the execution permission bit set (`chmod +x`on Unix-like systems) and should be in a directory listed in the PATH environment variable (usually Python's `site-packages`).

I agree there should be a more straight-forward instalation process. While that doesn't happen, please feel free to take a look at the next section and maybe consider contributing to this project.

## Did you find a bug or do you have a suggestion?

Please let me know, by opening a new issue or a pull request.
