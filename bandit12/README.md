<h1>Bandit 12</h1>
SSH using password found in bandit11.

```
ssh bandit12@bandit.labs.overthewire.org -p 2220
```

The next level password is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed.
First, revert the hexdump to gunzip extension.

```
xxd -r data.txt > data1.gz
```

Decompress the gzip file.

```
gzip -d data1.gz
```

Check the data1 file type.

```
file data1
```

Copy the file to a new file using the file type extension.

```
cp data1 data2.bz2
```

Decompress the bzip2 file.

```
bzip2 -d data2.bz2
```

Check the data2 file type.

```
file data2
```

Copy the file to a new file using the file type extension.

```
cp data2 data3.gz
```

Decompress the gzip file.

```
gzip -d data3.gz
```

Check the new file type of data3

```
file data3
```

Copy the file to a new file using the file type extension.

```
cp data3 data4.tar
```

Decompress the tar file.

```
tar -xvf data4.tar
```

Check the data5 file type.

```
file data5.bin
```

Change the file extension to the correct file type extension.

```
mv data5.bin data5.tar
```

Decompress the tar file.

```
tar -xvf data5.tar
```

Check the data6 file type.

```
file data6.bin
```

Change the file extension to the correct file type extension.

```
mv data6.bin data6.bz2
```

Decompress the bzip2 file.

```
bzip2 -d data6.bz2
```

Check the file type again.

```
file data6
```

Change the file extension to the correct file type extension.

```
mv data6 data7.tar
```

Decompress the tar file.

```
tar -xvf data7.tar
```

Check the data8 file type.

```
file data8.bin
```

Change the file extension to the correct file type extension.

```
mv data8.bin data8.gz
```

Decompress the gzip file

```
gzip -d data8.gz
```

Then, you can see the password in the file.
