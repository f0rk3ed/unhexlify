unhexlify
=========

Take data containing literal hex escapes, and replace them with the characters
they represent.

Requires python.

Examples:

```
~$ cat /tmp/data.txt
\x1CC51
~$ unhexlify /tmp/data.txt | hexdump -C
00000000  1c 43 35 31 0a                                    |.C51.|
00000005
```

You can also read from stdin using - or by specifying no files at all:

```
~$ cat /tmp/data.txt | unhexlify | hexdump -C
00000000  1c 43 35 31 0a                                    |.C51.|
00000005
```
