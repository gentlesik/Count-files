.. Count Files documentation master file, created by
   sphinx-quickstart on Sat Aug  4 20:40:31 2018.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Count Files
===========

A command-line interface (CLI) utility written in Python to help you
count files, grouped by extension, in a directory.

By default, it will count
files recursively in current working directory and all of its subdirectories,
and will display a table showing the frequency for each file extension (e.g.:
.txt, .py, .html, .css) and the total number of files found.

**Main functions:**

* counting files by extension and sorting results by frequency or alphabetically;
* file searching by extension, additionally: file sizes, preview for text files;
* total counting of all files or files with a specific extension.

**Features:**

* counting or searching files with a specific extension, files without an extension, all files regardless of the extension;
* recursive and non-recursive counting or searching;
* an option to include or exclude hidden files and folders while searching or counting;
* an option to process the file extensions with case-sensitive or case-insensitive mode;
* an option to turn off the program's operating indicator (feedback).

**Supported operating systems:**

Linux, macOS, Windows.

It may also be used on
iOS (iPhone/iPad) using the `StaSh <https://github.com/ywangd/stash>`_
command-line in the Pythonista 3 app.

**Supported Python versions:**

Python 3.6 and later

**Tested:**

* Linux Mint 19 "Tara", Python 3.6.5
* Windows 8.1 Professional, Python 3.6.0
* macOS 10.13.6 High Sierra, Python 3.7.0
* macOS 10.13.6 High Sierra, Python 3.6.6
* macOS 12.12.6 Sierra, Python 3.7.0
* macOS 12.12.6 Sierra, Python 3.6.6
* macOS 12.11.6 El Capitan, Python 3.7.0
* macOS 12.11.6 El Capitan, Python 3.6.6
* iOS 12.0 (Pythonista 3.2), Python 3.6.1
* iOS 9.3.5 (Pythonista 3.2), Python 3.6.1


**License:** MIT

**Source on GitHub:** `Project repository <https://github.com/victordomingos/Count-files>`_

**Contents:**

.. toctree::
   :maxdepth: 2

   installation
   howtouse
   examples

**Did you find a bug or do you have a suggestion?**

Please, open a new issue or a pull request to the `repository <https://github.com/victordomingos/Count-files>`_.


Search
------

* :ref:`search`
