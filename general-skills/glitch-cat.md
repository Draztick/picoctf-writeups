# Glitch Cat

## Description

Our flag printing service has started glitching! 

```
$ nc saturn.picoctf.net 53638
```

## Prerequisites

Have netcat or nmap (ncat) installed. Also, python3 is really nice to solve this quickly.

## Solution

Given the directions, I connected to the port on the associated server with netcat to view the output. The output of this service is the flag; however, a portion of it is a formula with some hex values surrounded by *chr(...)*. I immediately recognized this as python syntax, so I copied the output, openned a second terminal, dropped into a *python* interactive shell, and put the output of the service in a print() function. This would process the *chr(...)* functions on the hex values and convert them to their corresponding ASCII values. Once I hit enter, the plaintext flag was printed to screen and the problem was solved.