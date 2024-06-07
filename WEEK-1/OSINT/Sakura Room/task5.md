## Taunt
### Description -
- Background

Just as we thought, the cybercriminal is fully aware that we are gathering information about them after their attack. They were even so brazen as to message the OSINT Dojo on Twitter and taunt us for our efforts. The Twitter account which they used appears to use a different username than what we were previously tracking, maybe there is some additional information we can locate to get an idea of where they are heading to next?

We've taken a screenshot of the message sent to us by the attacker, you can view it in your browser here.


- Instructions

Although many users share their username across different platforms, it isn't uncommon for users to also have alternative accounts that they keep entirely separate, such as for investigations, trolling, or just as a way to separate their personal and public lives. These alternative accounts might contain information not seen in their other accounts, and should also be investigated thoroughly. In order to answer the following questions, you will need to view the screenshot of the message sent by the attacker to the OSINT Dojo on Twitter and use it to locate additional information on the attacker's Twitter account. You will then need to follow the leads from the Twitter account to the Dark Web and other platforms in order to discover additional information.

#### The first question was 
```
What is the attacker's current Twitter handle?
```
I provide us with a image taunt.png 

![Screenshot from 2024-06-07 13-39-37](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/444f90ee-3a6a-4433-adc3-a75af6babbd5)

I immediately googled @AikoAbe3 and found this [link](https://x.com/sakuraloveraiko?lang=en)

![Screenshot from 2024-06-07 13-41-39](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/173a86de-37a1-40ed-88df-d6cf299e44e0)

And got the answer
```
SakuraLoverAiko
```
#### The second question was
```
What is the URL for the location where the attacker saved their WiFi  SSIDs and passwords?
```
In the above image the attacker hinted us something like DEEPPASTE. I immediately opened tor brower and searched for DEEPPASTE links and found this [link](http://deepv2w7p33xa4pwxzwi2ps4j62gfxpyp44ezjbmpttxz3owlsp4ljid.onion). 

![Screenshot from 2024-06-07 13-55-21](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/96300855-3705-487f-b3b2-a2ef7aec3a41)

So I got the answer
```
http://deepv2w7p33xa4pwxzwi2ps4j62gfxpyp44ezjbmpttxz3owlsp4ljid.onion
```
#### The third question was 
```
What is the BSSID for the attacker's Home WiFi?
```
If you use the link above padded with md5 hash shown in the image you will get this link (http://deepv2w7p33xa4pwxzwi2ps4j62gfxpyp44ezjbmpttxz3owlsp4ljid.onion/show.php?md5=b2b37b3c106eb3f86e2340a3050968e2) searching it you will get something like this -

```
Saving here so I do not forget

School WiFi Computer Lab: 			GTRI-Device		GTgfettt4422!@
Mcdonalds: 					Buffalo-G-19D0-1        Macdonalds2020
School WiFi: 					GTvisitor		GTFree123
City Free WiFi: 				HIROSAKI_Free_Wi-Fi 	H_Free934!
Home WiFi: 					DK1F-G			Fsdf324T@@
```
The next flag calls for the attackers “HOME” BSSID, this sounds like a long shot but with modern wardriving/WAP mapping techniques, a lot can actually be dug up on a great service called (https://wigle.net). On twitter the Aiko posted this picture-

![Screenshot from 2024-06-07 14-37-38](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/93c58c7d-975c-4e8f-a274-b9d723281cdd)

we can just open basic search and manually scrolled over the map of japan and hit query and we get the answer
```
84:af:ec:34:fc:f8
```
















