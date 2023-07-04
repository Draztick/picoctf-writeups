# convertme.py

## Description

Run the Python script and convert the given number from decimal to binary to get the flag. Download Python script

## Prerequisites

Download the provided python script and ensure that python is properly installed.

## Solution

This can be solved in a similar way as one of the previous challenges. I started by running the provided python script, which asked me to convert 95 to binary. I then wanted to check if the number changes, so I used Ctrl+C to kill the program and ran it again and received 27 this time. Turns out, the number does change each time.

From here I opened a second terminal window and issued a base *python* command to open an interactive python shell. From there I typed the following into the python shell and got the answer, removing the 0b from the beginning.

```
bin(27)
```

Entering the answer 11011 was correct and the plaintext flag was printed to screen.