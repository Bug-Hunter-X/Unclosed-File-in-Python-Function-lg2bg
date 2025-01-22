# Unclosed File Bug in Python

This repository demonstrates a common but subtle bug in Python: forgetting to close a file after opening it.  This can lead to resource leaks, especially if the program handles many files or runs for a long time. The `bug.py` file showcases the error, while `bugSolution.py` presents the corrected version.

## Problem
The `function_with_unclosed_file` in `bug.py` opens a file but doesn't always close it, resulting in a file handle being left open after the function exits. This is particularly problematic if exceptions occur before the `f.close()` call.

## Solution
The `bugSolution.py` file provides a corrected implementation using a `with` statement. The `with` statement ensures that the file is always closed, even if exceptions arise.  This is the recommended and most Pythonic way to handle file I/O.
