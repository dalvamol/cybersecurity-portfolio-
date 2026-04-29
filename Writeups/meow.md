Hakeando maquina MEOW de Hack the Box

Procedimiento:

1. Desde Virtual Box ingreso a Hack the box, descargo el archivo de la VPN y la abro en Linux "sudo openvpn starting_points_us-starting-point-2-dhcp.ovpn" y dejo la vpn abierta en esa shell y abro otra pestaña.

2.Luego hago un mapeo inicial con nmap -sV "Ip que te dan al correr la maquina", esto con el fin de ver que nos arroja es escaneo.

El escaneo nos arroja lo siguiente:

└─$ nmap -sV 10.129.150.219                                   
Starting Nmap 7.98 ( https://nmap.org ) at 2026-04-28 22:03 -0400
Nmap scan report for 10.129.150.219
Host is up (0.10s latency).
Not shown: 999 closed tcp ports (reset)
PORT   STATE SERVICE VERSION
23/tcp open  telnet  Linux telnetd
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 17.15 seconds


Si analizamos esto podemos ver que el puerto 23/tcp está "open" y el servicio que corre allí es Telnet.

4. Ahora que sabemos que el servicio está abierto, vamos a intentarnos loguear, primero tiramos este comando telnet 10.129.150.219.

5. Efectivamente nos deja conectarnos y nos pide user, a lo que le indicamos root.

6. Nos deja entrar sin si quiera pedir una contraseña, lo cual es critico en un sistema.

7. Luego listamos con ls, para ver que archivos existen.

8. validamos que hay un archivo flag.txt, entramos en el con cat y cogemos la bandera.

Solución: b40abdfe23665f766f9c61ecba8a4c19

Conclusión:

La herramienta clave para encontrar está flag fue nmap, dado que, me permitió encontrar las vulnerabilidades que existían en la maquina con solo tener la ip.
