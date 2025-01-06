# Tcl Robust File Line Counter

This repository contains a Tcl procedure designed to count the number of lines in a file. The initial version contains a flaw in error handling and potential memory issues.  A corrected, more robust version is also provided.

## Bug Report

The original `count_lines` procedure fails to handle cases where the file does not exist or is empty. It also lacks robust error handling for potential issues during file I/O.  For extremely large files, storing each line in memory before counting can cause performance issues and even memory exhaustion. 

## Solution

The improved version uses `catch` to handle file opening errors and explicitly checks for empty files.  It processes the file line by line, avoiding unnecessary memory usage.