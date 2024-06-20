# Metasploitable-2
Metasploitable 2 - Exploiting NFS and cracking hashing with JohnTheRipper

I assigned Metasploitable an IP of 198.168.20.2. I assigned Kali and IP of 192.168.20.1.
![image](https://github.com/kofiarthurs/Metasploitable-2/assets/43903197/27bdc249-c890-41ec-803e-ad7c8f77fc0b) </br>
The ping scan only gets my host (Kali) IP. It shows the victim's IP (192.168.20.2) as down.
The -v stands for verbose, it shows every step the scan goes through.


<br>![image](https://github.com/kofiarthurs/Metasploitable-2/assets/43903197/1cd9f73b-99b1-43dc-8d72-37a1e082474e) </br>
-SL List Scan lists the whole IP range. It’s not meant to specify if a host is live or not. 


<br>![image](https://github.com/kofiarthurs/Metasploitable-2/assets/43903197/6ddf00c7-f0ef-4ca0-8315-f3f9ae5a770b)</br>
![image](https://github.com/kofiarthurs/Metasploitable-2/assets/43903197/7017d40d-ad5b-4475-8832-ce43c54cef65)</br>
This scan treats all hosts as online and looks for open ports. It only found ports for 192.168.20.2, indicating that it’s the only host on the network aside from the attacker. </br>
</br>


![image](https://github.com/kofiarthurs/Metasploitable-2/assets/43903197/ab2c300a-f109-4324-a0e2-89d7343be99a)
![image](https://github.com/kofiarthurs/Metasploitable-2/assets/43903197/4c3242f8-936c-4a1e-9705-dd5180a83f9e)
In this scan -O finds the OS version, -p- specifies all ports 65535, -sV finds the services and their versions. -sV has a version probe intensity 0-9, 7 is the default and 9 is the highest intensity. When experimenting with -sV 9 and 2 I received the same version results, indicating that the services versions were easy to find.

Nmap uses SYN Stealth scan to find open ports. It is stealthy because it doesn’t complete the TCP 3-way handshake. 

The default timing template is T3 which is a good balance of speed and stealth to avoid detection. The range is 0-5, 5 being the max.

NOTES PENDING
 
