## UNVEIL
Description- 
- Background

It seems the cybercriminal is aware that we are on to them. As we were investigating into their Github account we observed indicators that the account owner had already begun editing and deleting information in order to throw us off their trail. It is likely that they were removing this information because it contained some sort of data that would add to our investigation. Perhaps there is a way to retrieve the original information that they provided? 


- Instructions

On some platforms, the edited or removed content may be unrecoverable unless the page was cached or archived on another platform. However, other platforms may possess built-in functionality to view the history of edits, deletions, or insertions. When available this audit history allows investigators to locate information that was once included, possibly by mistake or oversight, and then removed by the user. Such content is often quite valuable in the course of an investigation. In order to answer the below questions, you will need to perform a deeper dive into the attacker's Github account for any additional information that may have been altered or removed. You will then utilize this information to trace some of the attacker's cryptocurrency transactions.

So the first question was -
```
What cryptocurrency does the attacker own a cryptocurrency wallet for?
```
So reading the description hinted that there can be some links at the attackers github page and heading twords that I found a repo named ETH which had a miningscript.md. If we click history on the right above this line, we can see that the file we are viewing was edited.  The edit history shows two commits to this file, one for create, and one for update. The update commit is the one we currently see above, which is an edit of the original one. 
![Screenshot from 2024-06-07 13-21-48](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/ac866fd3-b2a0-446f-93ed-8ae8bc0ca0dc)

So when I googled stratum://ethwallet.workerid:password@miningpool:port. I got the first answer
```
Ethereum
```
The second question was 
```
What is the attacker's cryptocurrency wallet address?
```
This answer is hidden in the above image itself.
```
0xa102397dbeeBeFD8cD2F73A89122fCdB53abB6ef
```
The third question was 
```
What mining pool did the attacker receive payments from on January 23, 2021 UTC?
```
 When I google this stratum://0xa102397dbeeBeFD8cD2F73A89122fCdB53abB6ef.Aiko:pswd@eu1.ethermine.org:4444 I go the mining pool to be 
```
Ethermine
```
The fourth and last question was -
```
What other cryptocurrency did the attacker exchange with using their cryptocurrency wallet?
```
After doing a lot of research I got to this [link](https://etherscan.io/) searching It with the above crypto wallet address I got on to this-
![Screenshot from 2024-06-07 13-33-58](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/3007f1b8-cc8b-4b32-bf69-075f85e4a0d7)

Hence I finally reached the answer
```
Tether
```

