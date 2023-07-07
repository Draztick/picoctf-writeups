# Glitch Cat

## Description

If you want to hash with the best, beat this test!

```
$ nc saturn.picoctf.net 52679
```

## Prerequisites

Have netcat or nmap (ncat) installed. Know how to perform an md5 checksum on your given operating system.

## Solution

Once connected to the port of the given server with nmap, the instructions say to input the md5 hash of a random string between single-quotes. The values between the single quotes differ at runtime. While this could be automated with python socket programming, this particular problem only requires 3 seperate checks to get a flag so it doesn't make sense to automate it in my opinon. Using the following syntax and replacing the value of the echo request 3 times, I was able to solve the problem, with the flag being printed after entering the third hash value.

```
echo -n "VALUE" | md5sum
```

Note: In Linux, a space and a dash (-) are included in the line when an md5sum is performed. These two characters should be omitted from the answer.