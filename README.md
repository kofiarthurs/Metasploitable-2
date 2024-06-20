# Metasploitable-2
<h1>Metasploitable 2 – Exploiting NFS and cracking hashes with JohnTheRipper</h1>

<h2>Description</h2>
In this lab, I exploit Metasploitable 2 (victim) using Kali (Attacker). I aim to scan the machine for vulnerabilities using NMAP and NESSUS, find the shadow file and crack the hashes.

I have assigned Metasploitable 2 an IP of 192.168.20.2 and Kali 192.168.20.1.

<h2>NMAP Scan</h2>
When scanning the victim, I’m looking for open ports, services and version numbers because older version might have vulnerabilities.</br>
![image](https://github.com/kofiarthurs/Metasploitable-2/assets/43903197/849dda80-e0e8-45c8-9431-8913bd07de69)
</br>
![image](https://github.com/kofiarthurs/Metasploitable-2/assets/43903197/c6930e2e-3978-4859-9cfa-1371001445ff)

<h2>Nessus Scan</h2>
The Nessus scan tells us that NFS is vulnerable. 
![image](https://github.com/kofiarthurs/Metasploitable-2/assets/43903197/a66fee9a-5a8c-4232-ab10-da2a989dc949)</br>
![image](https://github.com/kofiarthurs/Metasploitable-2/assets/43903197/a22511ce-f31f-4554-96ba-3b4d3305c3a6)</br>

<h2>Mounting NFS</h2>
I was able to mount NFS by making a directory on Kali and mounting it.</br>
![image](https://github.com/kofiarthurs/Metasploitable-2/assets/43903197/084d9355-0642-4f2e-8c05-a47ed294b343)</br>
![image](https://github.com/kofiarthurs/Metasploitable-2/assets/43903197/3a1c791c-70d7-4752-bdf8-7d8e9dc3c386)</br>

<h2>Hash Cracking</h2>
I found the hashes, copied them to a file on my Kali machine, and ran JohnTheRipper. </br>
![image](https://github.com/kofiarthurs/Metasploitable-2/assets/43903197/52a98255-741b-41e5-b9dc-06366b7988b7)</br>
![image](https://github.com/kofiarthurs/Metasploitable-2/assets/43903197/e720735c-17b3-45f7-9b2c-b3fd09d323fe)</br>
The root hash is salted, so I can’t crack it but I know the password to be msfadmin.
