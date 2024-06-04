## Matryoshka doll

Description - Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? 

 This challenge had the following image.

 ![dolls](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/eb6f3748-71de-4e32-a007-e93c5c9cfe1c)

 So the first thing that comes in my mind by reading the challs description is using binwalk tool 

 As the image says that the Matryoshka dolls are placed one inside another therefore I used binwalk tool as Binwalk is a tool for searching a given binary image for embedded files and executable code. Specifically, it is designed for identifying files and code embedded inside of firmware images. Binwalk uses the libmagic library, so it is compatible with magic signatures created for the Unix file utility.

![Screenshot from 2024-06-05 00-52-49](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/f89c2e5c-e023-4c43-9d4b-67996c95c552)

Hence it is clear that the image had some compressed data 

Now the question which comes in the mind is how to extract those datas for that we can read the man page of binwalk
```
man binwalk
```
it says that we can use the -e flag to extract the compressed data
using the command 
```
binwalk -e doll.jpg
```

![Screenshot from 2024-06-05 01-01-58](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/d204a296-621c-436d-add8-213ab428cc76)

we now get a new folder named _dolls.jpg.extracted opening the folder gives another folder named base_images which had a jpg image file 2_c.jpg

Again binwalking the image file had some compressed data  
 
again using the command 

```
binwalk -e 2_c.jpg
```
now it created another folder named _2_c.jpg.extracted which had another same folder named base_images which had another jpg image 3_c.jpg

Now simply repeating the above steps I got the flag.txt
```
picoCTF{e3f378fe6c1ea7f6bc5ac2c3d6801c1f}
```
Another way of doing this chall is by using the foremost tool using the command 
```
foremost doll.jpg
```
Now this creates a output folder in the current directory which has a zip file use unzip command to unzip the file and extract the image 2_c.jpg now we can apply foremost again on the 2_c.jpg and repeat the steps further to get the flag :)

