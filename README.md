# PHP File Handling Bug
This repository demonstrates a common error in PHP file handling: failure to check the return value of `fopen()` before proceeding. This can lead to unexpected behavior or crashes.  The `bug.php` file contains the faulty code, while `bugSolution.php` provides the corrected version.

## Description
The bug lies in the way the code handles potential errors when opening a file.  If the file doesn't exist, `fopen()` will return `false`, but the code doesn't explicitly check for this condition. This can result in subsequent operations on a `false` value, leading to errors or unpredictable outputs.

## Solution
The solution involves adding a check to see if `fopen()` successfully opened the file before attempting to process it.  The corrected code ensures robust error handling.