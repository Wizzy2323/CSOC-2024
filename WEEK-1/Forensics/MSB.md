## MSB  

Description-This image passes LSB statistical analysis, but we can't help but think there must be something to the visual artifacts present in this image... 

First of all I was curious about what is msb so I google it and found this on github-

![Screenshot from 2024-06-06 23-44-46](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/b955498d-acc8-4e40-86e9-ca257e0e4fbd)

Then through a lot of research I came across [sigbits](https://github.com/Pulho/sigBits) and using the following command I generated a output file which holds the flag
```
python3 sigBits.py -t=Msb Ninja-and-Prince-Genji-Ukiyoe-Utagawa-Kunisada.flag.png 
```
The output file was very large so the cat command could'nt help therefore I used the command 
```
cat output.txt | grep "pico"
```
But this spitted a huge amount of text this is because of the reason that their was no space in between words of the text due this it was problematic.But grep can used to output restricted to the matched string and using regex to add 50 characters after the "picoCTF"  

Using the command 
```
cat outputSB.txt | grep -o -E "pico.{0,100}"
```
I got the flag
## Flag
```
picoCTF{15_y0ur_que57_qu1x071c_0r_h3r01c_24d55bee}
```
