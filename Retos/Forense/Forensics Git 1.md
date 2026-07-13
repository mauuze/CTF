# Forensics Git 1

Primero vemos si el disco tiene particiones con el comando:

mmls disk.img

Y vemos que si tiene particiones:

<img width="744" height="192" alt="Screenshot_20260712_234029" src="https://github.com/user-attachments/assets/d79a2915-ec35-4b9f-8ad5-dde990a876b1" />

Nos quedamos con la particion que tiene como inicio 0001140736 y le hacemos una copia de los archivos a una carpeta llamada recovered1 con el comando:

**tsk_recover -e -o 0001140736 disk10.img recovered1**

y nos dirigimos a la direccion **recovered1/home/ctf-player/Code/secrets**, a difencia del reto Forensics Git 0 que ademas del .git habia una note.txt aqui solo esta el **.git**

Utilizamos el comando:

**git log --all --oneline**

y nos sale lo siguiente:

<img width="817" height="56" alt="Screenshot_20260712_234844" src="https://github.com/user-attachments/assets/fb83a2ce-af48-40ee-96ed-11f1b2f110a9" />

Tenemos la pista de **How can you checkout the files of a previous commit?**, por lo que nos movemos un commit anterior con el comando:

**git checkout 177789a**

Si observamos los archivos de la direccion **recovered1/home/ctf-player/Code/secrets**, ahora tambien nos sale un archivo flag.txt si lo abrimos obtenemos la flag:

**picoCTF{g17_r3m3mb3r5_d4ddf904}**

Subimos la flag a picoctf y listo.

<img width="1369" height="92" alt="Screenshot_20260712_235334" src="https://github.com/user-attachments/assets/8f0e7069-18ed-417f-a505-469a527993e0" />
