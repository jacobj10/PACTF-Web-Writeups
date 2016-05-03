#A Fierce Attacker Problem (80)
##Intelligence states that the flag is located on a server with the domain ‘pactf2.tk’ on a secret sub-domain. Can you find the correct sub-domain?

The hint gives it away : Take a guess. Or find someone fierce instead.

Googling of Fierce/Fierce Attacker/Fierce Attacker Domain leads you to find Fierce, a scanning tool on linux platforms.

Follow the steps to install fierce:

https://www.aldeid.com/wiki/Fierce

Run on the command line:

```shell
>fierce -dns pactf2.tk
```

and you will be directed to vpn.pactf2.tk which contains the flag.

Flag: CJY0n9d1cZHkuEkEsF2U5sf1Aqh0TQ
