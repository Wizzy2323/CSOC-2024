## Enhance!

Description- Download this image file and find the flag.

This challenge can easily be sloved using cat command. Once we 
```
cat drawing.flag.svg
```
we get to see

![Screenshot from 2024-06-06 00-47-59](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/dcb2a14c-fa77-4591-89d2-0b7c925eda02)

We can easily see the flag here but for more clearity we can use the command -
```
cat drawing.flag.svg | grep "</tspan>"
```
we get -

![Screenshot from 2024-06-06 00-50-28](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/744bbe61-b5b5-4a8d-b46e-cb981019af63)

Hence the flag is 
## Flag
```
 picoCTF{3nh4nc3d_24374675}
```



