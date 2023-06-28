# Wave a flag

## Description

Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...

## Prerequisites

Download the program specified (called "warm") in the description.

## Solution

To find out the type of file that warm is, I began by issuing a *file* command.

```
file warm
```

![file command output](../images/wave-a-flag-file.png)

From this output I can see that the file is a 64-bit ELF file, meaning it is an executable. To execute it as intended, we need to make sure it has execute permissions for the current user. This can be checked by issuing a *ls* command with an -l switch to specify the list format and the file name to show only that file. I can see that the file only has read-write permissions for my current user.

I want to ensure that the current user has the permissions to execute the file. I thus issue a *chmod* command followed by u+x, specifying that we want to give the owner of the file executable permissions, and then the name of the file. Then I make sure that the change worked as intended by issuing the same *chmod* command and comparing the results.

![permissions changing](../images/wave-a-flag-permissions.png)

Once execute permissions have been set, we can execute the file by prepending the name of the file with a period and a forward slash:

```
./warm
```

Once executed, the program asks us to pass a -h switch as an argument to learn what it does.

```
./warm -h
```

This output returns a message containing the plaintext flag.

![solution](../images/wave-a-flag-solution.png)