# CTF KURS

#### CTF'orno? Fra scan til pwn.
#### https://github.com/theodorsm/itemize-ctf-course21

```
                                                                ................................................................................
                                                                ....................'''.'''''.',.','''''','..''..''''''''..''...................
                                                                .................',,,,,,,',;,';;,,;;,;;,;;;,,;;,,,,,,,,,,',;,','................
                                                                ..............'''',,''''''''''''''''',,''',,',,''''''''''''''''''''.............
                                                                ...........';;';;,;;,,,,;,,;;',;;',;,';;,,;;,;;''';;,,;;',:,';;,,;;'''..........
                                                                ..........',;,',;,;;,,,,,,,;;',;,',;,,;,,,;;,;,,,,;;',;;',;,';;,,;;',;'.........
                                                                .........'''''''''','''',,'''''''''''''''',,',,''''''''''''''''''',,'''.........
                                                                ........;;,'',,,,,,,,',,;;,,,,,,,,;,';;,',;;,;;,;;,;;,,;;,'',,,,,;;,,,,;'.......
                                                                ........,,,,''''','',,,';;,''',,,,,,',,,'',,,;;,,,',,,',,',,'','',;,'',,'.......
                                                                ........'''''''''',,,,'.'''.''...'..........'''..'''..'.',,,''',,,''''''........
                                                                .......':;,,:;,;:,,;;;;'................................';;;;,';:,,,,,,,'.......
                                                                .......',,,,,,',,,;;;,,..........''''''''''''''''''''...';;,,,,;;,,,,,,,'.......
                                                                .......';,,,,,,,;,;;,,,.........''''''''''''''''''''''..',,,;,;;;;,,,,,;,.......
                                                                .......,::;;c:;:c;;::::'........''''''''''''''''''''''..,:;;c:;::::;;;;c;.......
                                                                .......,;,;;;;;;;;;:;;,.....'...........................',;;;;;::;;;;;;;,.......
                                                                .......,::;;::;;:;;::;;'...,,,'.........................'::;::;:::::;;::,.......
                                                                .......,cc;:lc:cl:;cc:;,..';;;;;;;;;'..',,,,,,,,,,,,,,..'cc::c::c:cc::cc,.......
                                                                .......,::;::;;::;;::;;'..,;:;;;;;;;'..,::::;::::;;::;'.';;;;:::c:;:;::;,.......
                                                                .......;cc::::::::clc::'..,:::::::::,..,::;;::::::::;;'.'::::c::::::::::,.......
                                                                .......;llccccccccclcc:,..':::::::::,..',,,,,,,,,,,,,'..,:cccccccccc::::;.......
                                                                .......;c::cc:cc::clc::'...,:ccccccc:,'.'...............'::c::::cc::c:cc;.......
                                                                .......;llccolcllccolll,....,:clcccccccccccc:'.'::::::'.,ccclolcloccollo:.......
                                                                .......;llllolcllllolll,.....';cccccccccccccc'.,llllll,.,clclolllollollo:.......
                                                                .......;lccclcclcclllcc,.......',;:ccccccccc:'.,cllllc,.,cllclccclcclcll:.......
                                                                .......:oolodolodolooll;............'',,,,''...',;;;;,'.,odoloollloooloo:.......
                                                                .......:oolooolooolooll;'''''''''''''''''''''''''''''''';lollooloollllloc.......
                                                                .......:olllllllllllolllllllllllllllllllllllllccllllllllllollollllllllll:.......
                                                                .......;ooooooooodooddoodoodoodooddoodolllooooooddoooodolddooddlllllllll;.......
                                                                .......'cllllolloollolllooooooolloollooloolllllloollllolloollolllllllll:'.......
                                                                ........'cllooodolollllooolllllllllllllllloollooloolloooollooollllllolc'........
                                                                .........':odooddodooloodoooooooooooooooooodolddoodooddodooodooooooolc'.........
                                                                ...........,cloooloolllloolllllllllllllloololllllllooooolllooololllc,...........
                                                                .............';cloooooolollllooloooooooodolloooloooloolloollooool:,.............
                                                                ................,;:ccllllllclolclollollllllllllllolclollolccc:;,................

```


##  ITEMIZE???

### itemize.no

#### Sikkerhetsmilj?? p?? NTNU!

- Ukentlige arrangementer (kurs, CTF, org.)
- Frivillig, ??pen for alle (ikke bare abakuler)
- Lav terskel
- Pizza & CTF (typ annenhver uke)
- Kan ogs?? jobbe p?? nettside/interne prosjekter!

Sjekk ut kalender p?? itemize.no

## Hva er CTF?

### Classic

_Jeopardy_: konkurranse div. utfordringer. tidsbegrenset.
_Attack-defense_: to like set med maskiner med innebygde s??rbarheter.

### Wargames

Jeopardy bare der tiden ikke g??r ut. Oppgavene bygger p?? hverandre gradevis.

### Typer oppgaver

- Crypto
- Reverse
- Misc
- Forencics
    - Stego
    - Crash dumps
- Web
- PWN

## Motivasjon?

- Hobby.
- Jobb/karriere.
    - Pentester
    - Sikker applikasjonsutvikling
    - bug-bounty
- "Nettvett"
- Nysgjerrig.
- Dopamin

## CTF vs. IRL

### Akt??rer

- Nation state, APT
- Organiserte (kriminelle, aktivister)
- "hacker" (individer)
- "script kiddie"

###s??rbarheter.

- Zero day
- Common Vulnerabilities and Exposures (CVE)

## Scan

Opportunistisk vs. rettet

??pne porter?
*80/433*: HTTP/HTTPS
__Kan bruke web-applikasjon som inngang til maskin.__

```
nmap -p- 172.17.0.2
```

<!--
Vise eks:
Scanne docker container:
hostname -I
namp -p- IP
Bruke Burp til ?? vise cookie monster
Sp??rr om noen i salen ser l??sning.
-->

## Web

### OWASP 10:
- Injection -> SQLi, CMDi
```
navn = get_user_input()
os.system("echo 'Nice to meet you:\n'")
os.system("echo " + name)

==============

INPUT:
> bashgobrr; ls
Nice to meet you:
bashgobrr
drwxr-xr-x 4 theodor users 4096 Sep  8 16:46 .
drwxr-xr-x 3 theodor users 4096 Aug 31 01:33 ..
-rw-r--r-- 1 theodor users 3456 Sep  6 22:46 secretfile
```

- Broken Authenticaiton
- Sensitive Data Exposure
...
- Security Misconfiguration -> LFI
```
www.somesite.com/index.html/../../../etc/passwd
```
- Cross-Site Scripting XSS


BURPSUIT ER DIN VENN!

## Web - Oppgaver

level 0-9:
https://overthewire.org/wargames/natas/

### Tips and tricks:

- https://ctf101.org
- https://gchq.github.io/CyberChef/

## Gjennomgang!

## pwn

 -------------------
< Now youre fucked >
 -------------------

S??rbarhet i web => shell => admin tilgang

### PRIVILEGE ESCALATION

- Unytte konfigurasjonsfeil
    - brukerrettigheter
    - programmer


## pwn-Oppgaver

*Kjent med UNIX terminal:*
overthewire Leviathan

*Vil bli bedre kjent med UNIX terminalen:*
overthewire Bandit

## Gjennomgang!

## Knytte det hele sammen.

## Resurrser

- https://overthewire.org
    - Wargames, god start p?? UNIX, web, binary pwn.
- https://picoctf.org
    - Starter CTF
- https://hackthebox.eu
    - Litt mer utfordrende, maskiner tilgjengelige for pwn.
- http://smashthestack.org
    - "Old school" wargames
- https://ctf101.org
    - Wiki, type oppgaver
- https://missing.csail.mit.edu/
    - L??re UNIX, git, vim

#### YouTube kanaler:
- *LiveOverflow*
    - div. oppgaver og cybersecurity stuff
- *Jon Hammond*
    - Gjennomgang av CTF'er, div tutorials
- *IppSec*
    - HTB gud!
