# strings it

## Description
Can you find the flag in file without running it?

## Prerequisites
Download the provided file and have binutils installed if not already on your system.

## Solution

I have previously used strings in some reverse engineering work and so I already had an idea of what I needed to do. Also, give that we know the flag format, it is easy to grep for the desired information to get the answer quickly. I solved this by downloading the file called strings, provided by the problem, and then issued the following in the terminal:

```
strings strings | grep picoCTF
```

This revealed the flag in plain text and solved the problem.