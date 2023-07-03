# Bases

## Description

What does this bDNhcm5fdGgzX3IwcDM1 mean? I think it has something to do with bases.

## Prerequisites

Some method of decoding base64 encoded messages.

## Solution

My preferred method to decode base64 encoded messages is using the Linux command line. In most, if not all distros, base64 comes as a preinstalled program and it has a really simple syntax. To decode, I pipe the base64 encoded message into the base64 program with the -d flag to decode.

```
echo "bDNhcm5fdGgzX3IwcDM1" | base64 -d
```

Inserting the returned string into the standard picoCTF{...} flag format solves the problem.