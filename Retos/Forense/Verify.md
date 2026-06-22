# Verify
**People keep trying to trick my players with imitation flags. I want to make sure they get the real thing! I'm going to provide the SHA-256 hash and a decrypt script to help you know that my flags are legitimate.**

Nos conectamos al servidor que nos da picoCTF, vemos que contiene los siguiente:

<img width="302" height="36" alt="Screenshot_20260621_193907" src="https://github.com/user-attachments/assets/10939c6e-238c-47aa-82c3-4d52dc4afd89" />

En la carpeta files nos encontramos con muchisimos archivos, una opcion para resolver este ctf seria ir probando uno por uno, pero como como tenemos el checksum del archivo objetivo pódemos utilizar el siguiente comando:

**sha256sum /home/ctf-player/drop-in/files/* | grep 55b983afdd9d10718f1db3983459efc5cc3f5a66841e2651041e25dec3efd46a

Eso nos entrega el archivo a deesencriptar:

**55b983afdd9d10718f1db3983459efc5cc3f5a66841e2651041e25dec3efd46a  /home/ctf-player/drop-in/files/2cdcb2de**

Desencriptamos con 

**./decrypt.sh files/2cdcb2de**

Y obtenemos la ctf

**picoCTF{trust_but_verify_2cdcb2de}**

Subimos la flag a picoctf y listo.

<img width="970" height="114" alt="Screenshot_20260621_195809" src="https://github.com/user-attachments/assets/6aa224fd-4bf6-4a3a-a6e6-10e9438a214c" />
