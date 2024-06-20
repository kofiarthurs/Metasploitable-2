<h1>Metasploitable 2 – Exploiting NFS and cracking hashes with JohnTheRipper</h1>

<h2>Description</h2>
In this lab, I exploit Metasploitable 2 (victim) using Kali (Attacker). I aim to scan the machine for vulnerabilities using NMAP and NESSUS, find the shadow file and crack the hashes.
</br>
</br>
I have assigned Metasploitable 2 an IP of 192.168.20.2 and Kali 192.168.20.1.

<h2>NMAP Scan</h2>
When scanning the victim, I’m looking for open ports, services and version numbers because older version might have vulnerabilities.</br>
<img src="https://imgur.com/4Kynz2B.png" height="80%" width="80%"/>
<img src="https://imgur.com/JSxWvml.png" height="80%" width="80%"/>
<h2>Nessus Scan</h2>
The Nessus scan tells us that NFS is vulnerable. </br>
<img src="https://imgur.com/BBKKWWS.png" height="80%" width="80%"/>
<img src="https://imgur.com/Ob45ue4.png" height="80%" width="80%"/>

<h2>Mounting NFS</h2>
I was able to mount NFS by making a directory on Kali and mounting it.</br>
<img src="https://imgur.com/L2vZfwT.png" height="80%" width="80%"/>
<img src="https://imgur.com/HwBj0Rn.png" height="80%" width="80%"/>

<h2>Hash Cracking</h2>
I found the hashes, copied them to a file on my Kali machine, and ran JohnTheRipper. </br>
<img src="https://imgur.com/OLZku0F.png" height="80%" width="80%"/>
<img src="https://imgur.com/vT2gLvo.png" height="80%" width="80%"/>
The root hash is salted, so I can’t crack it but I know the password to be msfadmin.

