## Information

Description - Files can always be changed in a secret way. Can you find the flag? cat.jpg

So this challenge had a jpg image of a cat.

![image](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/20ec393f-f596-49ca-bc70-1cdc99b409ce)


For solving Forensic challs my few go to go tools are
file
binwalk
exiftool
steghide 
stegseek
zsteg
etc.


So I first used the file command on the image to check if the image is really a jpeg image or not 
![image](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/647e3b5d-435e-4de3-b6a6-8d84f4b9b74d)

hence everything was perfect here!

Then I used binwalk on the image  

![image](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/90d714f5-325e-45d1-ba34-7fe7b8db0d19)  

but everything seemed fine.

Then I used the exiftool command  

![Screenshot from 2024-06-05 00-24-35](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/1a746766-bb59-4524-b040-564ed4454e77)

Here the encrypted license seemed intresting to me, applying the base64 decription using the command
```
echo cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9 | base64 -d

```
I got the flag 
```
picoCTF{the_m3tadata_1s_modified}
```

Another method to solve this chall is by using a image viewer like gwenview or an image editor like photoshop or gimp

By searching in the details of the image one can easily find the base64 encripted license.






