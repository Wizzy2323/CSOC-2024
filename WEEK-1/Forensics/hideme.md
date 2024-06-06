## Hideme

Description-Every file gets a flag. The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye here.

First of all I used file command and then exiftool on the flag.png and found nothing. Using binwalk was the key after using binwalk I got this-

![Screenshot from 2024-06-06 23-29-06](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/f8490e31-b525-45b0-9841-5f8b76bb8770)

then I used the following command to extract the embedded data -
```
binwalk -e flag.png
```
After this I got a directory named _flag.png.extracted which had a secret dir which had an image having the flag

![Screenshot from 2024-06-06 23-31-21](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/eba9edac-1722-407d-8f57-1e457e8281f6)

## Flag
```
picoCTF{Hiddinng_An_imag3_within_@n_ima9e_ad9f6587}
```




