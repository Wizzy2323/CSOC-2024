## advanced-potion-making
Description- Ron just found his own copy of advanced potion making, but its been corrupted by some kind of spell. Help him recover it! 

By looking at the header of the file it seemed to be a corrupted file so I decided to copy the headers and ask chatgpt for the correct header and it gave me this -

![Screenshot from 2024-06-06 01-03-01](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/807b5f4a-fd44-4108-ae5e-8ccbdca12b45)

So I decided to change the file header using a hex editor.

I substituted the hex values provided by the chatgpt and got a result as-

![Screenshot from 2024-06-06 01-08-19](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/15fba295-ff4a-4a34-a6e6-ee9d52b8df6c)

by applying all sorts of trivial forensics methods I got nothing then I decided to go for an online website named Aperi'Solve 

But before uploading the file we need to rename the file and add the .png extension at its end!

After uploading the file we got-

![Screenshot from 2024-06-06 01-12-42](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/ed9bf63d-9e80-42c5-a21c-ba89953dd3cf)

Hence the flag can be clearly seen 
## Flag
```
picoCTF{w1z4rdry}
```
