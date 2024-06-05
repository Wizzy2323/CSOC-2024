## tunn3l v1s10n

Trying all sorts of different methods did'nt gave any clues.But opening the image in the image viewer gave this -

![Screenshot from 2024-06-05 23-13-56](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/c1416ddc-2ad3-4c07-81d4-018f581a6e10)

So their is a possibility that the image file may be corrupted and requires some fixing ;)

I already had okteta installed so I opened the image with the command 

```
okteta tunn3l_v1s10n
```

By watching at the headers of the image file it seemed to be a BMP (bitmap file format). For the confirmation I asked chatgpt and it gave me the same file format. 

By looking closely at the first few hex values I suspected some of the corrupted symbols

![Screenshot from 2024-06-05 23-22-32](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/e8ee2e00-38d5-4e17-92df-23eaa9af9b2b)

After this I asked chatgpt to provide me with correct headers of the BMP file format and it gave me this 
```
42 4D 8E 26 00 00 00 00 00 00 36 00 00 00 28 00 00 00 20 03 00 00 68 02 00 00 01 00 18 00 00 00 00 00 58 26 00 00 13 0B 00 00 13 0B 00 00 00 00 00 00 00 00 00 00
```
After this I interchanged the hex values of the first row third and fourth column with the values provided by chatgpt.Now you would be wondering why only the hex values of first row third and fourth column it is because their symbols seemed corrupted.

After doing so and saving the file the image opened like-

![Screenshot from 2024-06-05 23-33-07](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/e57ddc77-88bf-4f2e-bdc4-45f3871a1e8c)

Now applying all the forensics command line tool on the new image did'nt gave any sort of clue.But the challenge name had something to do with it?

Then I decided to change the dimensions of image using okteta hex editor. But for that we first need to find the hex values which stores the dimensions of the image.

For that we need to get the exact dimensions of the image hence I used file command - 

![Screenshot from 2024-06-05 23-42-32](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/9c8f5855-cb8b-4055-919a-614826aa6523)

I changed the given dimensions to hex values and comapared it with the values of the hexeditor to get the position the hex values storing the dimensions of the image.

After this I started playing with the dimensions substituting the hex values more than the previous for increasing the height of the image. Note 306 is the original height of the image.

After a lot of attempts my changing the height of the image to 900~0x384 I go the image -

![Screenshot from 2024-06-05 23-58-27](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/5aa42f17-12ae-44a1-8e7d-a9aa4dbfe227)
## flag
```
picoCTF{qu1t3_a_v13w_2020}
```

