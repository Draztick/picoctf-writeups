# Warmed Up

## Description
What is 0x3D (base 16) in decimal (base 10)?

## Prerequisites
No major prerequisites. This can be done by hand, but python or an online decoder tool would make it easier.

## Solution

I could have used an online decoder, but python3 has a built in way to convert from base16 to base10 with a single line. I chose to use this method instead. I started python3 by entering *python* into the terminal, and then typed the following to do the converstion.

```
int('3D',16)
```

Taking the base10 output from this function and placing it into the picoCTF{...} flag format solves the problem.