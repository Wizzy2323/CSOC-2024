## RECONNAISSANCE
Description-
- Background

It appears that our attacker made a fatal mistake in their operational security. They seem to have reused their username across other social media platforms as well. This should make it far easier for us to gather additional information on them by locating their other social media accounts. 
- Instructions

Most digital platforms have some sort of username field. Many people become attached to their usernames, and may therefore use it across a number of platforms, making it easy to find other accounts owned by the same person when the username is unique enough. This can be especially helpful on platforms such as on job hunting sites where a user is more likely to provide real information about themselves, such as their full name or location information.

 

A quick search on a reputable search engine can help find matching usernames on other platforms, and there are also a large number of specialty tools that exist for that very same purpose. Keep in mind, that sometimes a platform will not show up in either the search engine results or in the specialized username searches due to false negatives. In some cases you need to manually check the site yourself to be 100% positive if the account exists or not. In order to answer the following questions, use the attacker's username found in Task 2 to expand the OSINT investigation onto other platforms in order to gather additional identifying information on the attacker. Be wary of any false positives!

The username SakuraSnowAngleAiko can be searched using blackbird using the following command-
```
python3 blackbird.py -u SakuraSnowAngleAiko
```
In the result 

Out of the above links only the [github](https://github.com/sakurasnowangleaiko) link was active

In the link we have pgp repository which contains a public key which was base64 encrypted the pgp key was-

-----BEGIN PGP PUBLIC KEY BLOCK-----

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

23pRnPKc+41cwL3oq8yb/Fhj+biohgIp

=grbk

-----END PGP PUBLIC KEY BLOCK-----

use the command or use the cyberchef for more better
```
echo ..theabovetext.. | base64 -d
```
The resulted email was 

```
SakuraSnowAngel83@protonmail.com
```
For the next part I googled the username SakuraSnowAngleAiko and it gave the following result

![Screenshot from 2024-06-07 01-59-25](https://github.com/Wizzy2323/CSOC-2024/assets/159465554/249101ae-62df-4357-9d1e-2acca41c21b9)

The full name was 
```
Aiko Abe
```

