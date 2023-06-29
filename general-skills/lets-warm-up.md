# Let's Warm Up

## Description

If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?

## Prerequisites

No resources required as conversion can be done by hand with a reference to ASCII table, however, Python 3 or an online hex to ascii converter would be nice to have.

## Solution

While I could find an online hex to ascii converter, Python has a super simple oneliner that will do the work for me, so I opted to go with this method.

```
bytes.fromhex('70').decode('utf-8)
```

This returns the string 'p', which is the flag when applied to the standard flag format for picoCTF. 

picoctf{p}