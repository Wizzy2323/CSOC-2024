## MacroHard WeakEdge

Description - I've hidden a flag in this file. Can you find it? Forensics is fun.pptm

After downloading and opening the pptm I started applying all the trivial methods of forensics.

But when I used binwalk I got amazing stuffs.

![Screenshot from 2024-06-06 00-29-37](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/0d1597e3-81a3-4e31-97ab-33d538ca847a)

again using the command 
```
 binwalk -e Forensics\ is\ fun.pptm 
```
I extracted all the data and got a hidden.txt file. Which had base64 encoded flag

Another methods to extract the embedded data are-
```
unzip Forensics\ is\ fun.pptm
7z x Forensics\ is\ fun.pptm
```
## Flag
```
picoCTF{D1d_u_kn0w_ppts_r_z1p5}
```




