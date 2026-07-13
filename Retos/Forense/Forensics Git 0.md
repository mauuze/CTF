# Forensics Git 0

Primero vemos si el disco tiene particiones con el comando:

**mmls disk.img**

Y vemos que si tiene particiones:

<img width="715" height="190" alt="Screenshot_20260712_231641" src="https://github.com/user-attachments/assets/610eeadc-9a9f-48da-996a-49b8ef7b77b8" />

Nos quedamos con la particion que tiene como inicio **0001140736** y le hacemos una copia de los archivos a una carpeta llamada recovered con el comando:

**tsk_recover -e -o 0001140736 disk10.img recovered**

Mirando un poco en lo que recuperamos si llegamos hasta la parte de **recovered/home/ctf-player/Code/secrets** hay un archivo llamado note.txt que contiene lo siguiente:

**The picoCTF flag format is 'picoCTF{}' where there is some leetspeak phrase in between the curly braces**

Que no da muchas pistas de la flag.

Con el comando ls -la vemos que hay un archivo .git que indica que hay un respositorio, utilizamos un comando para ver los commits del repositorio:

**git log --all --oneline**

Y obtenemos lo siguiente:

**327681b (HEAD -> master) Wrap this phrase in the flag format: g17_1n_7h3_d15k_041217d8**

Aqui ya vemos una parte de la flag, la flag completa es la sigueinte:

**picoCTF{g17_1n_7h3_d15k_041217d8}**

Subimos la flag a picoctf y listo.

<img width="1372" height="88" alt="Screenshot_20260712_233038" src="https://github.com/user-attachments/assets/4869b30f-1fbd-4547-acfd-29e98ef9f183" />
