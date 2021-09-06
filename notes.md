# CTF KURS

#### CTF'orno? Fra scan til pwn.

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


## Hva er CTF?

### Classic

_Jeopardy_: konkurranse div. utfordringer. tidsbegrenset.
_Attack-defense_: to like set med maskiner med innebygde sårbarheter.

### Wargames

Jeopardy bare der tiden ikke går ut. Oppgavene bygger på hverandre gradevis.

## Motivasjon?

- Morsom hobby.
- Jobb/karriere.
- "Nettvett"
- Nysgjerrig.
- Bli bedre til å lagre sikre løsninger. mer og mer digital blabla

## CTF vs. IRL

Aktorer/sårbarheter.

## Scan

Opportunistisk vs. rettet

Åpne porter?
*80/433*: HTTP/HTTPS
__Kan bruke web-applikasjon som inngang til maskin.__

```
nmap -p- <IP>
```

#### 172.17.0.2

<!--
Vise eks:
Scanne docker container:
hostname -I
namp -p- IP
Bruke Burp til å vise cookie monster
Spørr om noen i salen ser løsning.
-->

## Web

## pwn

```
  -------------------
 < Now youre f*cked >
  -------------------
        |  ^__^
         <  (oo)\_______
             (__)\       )\/\
                 ||.---w |
                 ||     ||
```

Sårbarhet i web gir tilgang på maskin. Må eskalere priv.

## Knytte det hele sammen.


## Oppgaver

### overthewire.org

Leviathan: suid og priv-esc
Natas: web 0 - 10
10 -> overgang til priv esc.

Noen pico el. web oppgaver?

## Resurrser

hackthebox.eu
overthewire.org
https://missing.csail.mit.edu/
https://ctf101.org/web-exploitation/overview/

LiveOverflow (YouTube)
Jon Hammond (YouTube)
IppSec (YouTube)
