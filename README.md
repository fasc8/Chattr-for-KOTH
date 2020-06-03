# Chattr-for-KOTH

The twist with this chattr binary is that you can specify a username and a file name at compilation.

Then whenever someone tries to do (in this example the filter is made for king.txt)

```bash
chattr +i /root/king.txt
or
chattr -i /root/king.txt
```
your specified name will be written in that file before or after it is made immutable.
So you can easily stay king. You just have to exchange the original chattr binary with this one.

It will also only target the specified file. So it should stay pretty undetected...

## Compilation
```
gcc chattr_borked.c -o chattr_borked
```
