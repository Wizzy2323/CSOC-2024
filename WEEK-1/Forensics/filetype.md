## File Types

Description- This file was found among some files marked confidential but my pdf reader cannot read it, maybe yours can.

We were give a pdf file named flag.pdf.I used the file command to check the file type and it gave a shell archive text

After that I used the cat command and found out this-

![Screenshot from 2024-06-06 22-34-26](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/9e3ce278-ee4a-4f74-af63-5f0e2936a258)

The starting few comments told some instructions to perform. Therefore I copied the file to another file using the command 
```
cp Flag.pdf flag.sh
```

Note that I used the .sh extension because it was a shell archive and then gave the execution permission
```
chmod +x flag.sh
```
then we can execute the it using 
```
./flag.sh
```
Now we have an extracted flag file :)

After this I started using all the trivial forensic method on flag file and at the end binwalk worked. Therefore I used the following command to extract the embedded files-
```
binwalk -e flag
```
Now I move the directory named _flag.extracted and found a file named 64 and then I used the file command again and found out that it had gzip compressed data. I had already encountered a same chall in over the wire bandit so after this it was much easy for me. Now I used the following command to extract the embedded data-
```
gzip -d 64
```
The extracted folder contained a file named flag

Again using the file command on flag gave that it was an lzip compressed data. Then I used the following command to extract the embedded data-
```
lzip -d -k flag
```
Now I found a file named flag.out and again using the file command I found that it was LZ4 compressed data, so I used the following commands to extract the data-
```
lz4 -d flag.out flag2.out
```
Now this created a file named flag2.out and then I found that it was LZMA compressed data and then I used the following commands-
```
lzma -d -k flag2.out
```
this created file with unknown suffix so I used the file command and found that it was LZMA compressed Now the unknown suffix did'nt allowed the above command to execute so I renamed the file to file3.lzma and then used the above command again on the same file and found a file named flag2.

Again using the file command returned that it had LZOP compressed data so for this I used the following command after changing the extension of the file to lzop
```
lzop -d -k flag2.lzop -o idk
```
Now I got file named idk and again found out that it was lzip compressed so I used the command -
```
 lzip -d -k flag3
```
It created a file named flag3.out and I then found out that it was XZ compressed changing the extension to .xz and applying the command 
```
xz -d -k flag3.xz
```
Now I got a file named flag3 which had some ascii text after converting then I got the flag

## Flag
```
picoCTF{f1len@m3_m@n1pul@t10n_f0r_0b2cur17y_347eae65}
```

