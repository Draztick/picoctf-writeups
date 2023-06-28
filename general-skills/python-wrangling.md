# Python Wrangling

## Description

Python scripts are invoked kind of like programs in the Terminal... Can you run this Python script using this password to get the flag?

## Prerequisites

Download the python script, the encoded flag file, and the plaintext password text file.

## Solution

 Once downloaded, I checked a couple of things about the python file to determine if it is self-executable, or if I have to use the python program directly from the terminal.

Python scripts can be executed by first issuing the python command to specify the program used to interpret the file. On most modern Linux distributions, this is done by simply specifying *python* followed by the script name. Issuing this against the ende.py script displays some usage information about the file.

![ende.py usage info](../images/python-wrangling-usage.png)

From this output I inferred two things: the -e switch likely means encrypt while the -d switch likely means decrypt. Since the flag is encrypted, we will likely want to use the -d switch to reverse the encryption.

Now, since they include the pw.txt file and specified that it has a password in the description, I used the *cat* command on the pw.txt file provided to reveal the plaintext password.

![cat password out to terminal](../images/python-wrangling-pw-out.png)

Once I pulled all of it together and input the password I was able to decrypt the flag.

```
python ende.py -d flag.txt.enc
```

![decrypt passowrd](../images/python-wrangling-1.png)