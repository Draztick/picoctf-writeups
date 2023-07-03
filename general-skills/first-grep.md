# First Grep

## Description

Can you find the flag in file? This would be really tedious to look through manually, something tells me there is a better way.

## Prerequisites

Download the provided file, named file. Need the ability to output the file contents and search the output of the file. With Linux, this requires *cat* and *grep* respectively, although this is solvable in Windows as well.

## Solution

This is also an easy flag to obtain. You start by outputing the content of file using the *cat* command. Then you pipe standard output into *grep* searching for the picoCTF flag format.

```
cat file | grep picoCTF
```

This reveals the plaintext flag and solves the problem.