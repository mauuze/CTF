# information

**Files can always be changed in a secret way. Can you find the flag?**

Descargamos la imagen:

<img width="2560" height="1598" alt="cat" src="https://github.com/user-attachments/assets/7a24a6f6-d601-4ab9-a56c-eecd47659fc6" />


Sacamos los metadatos con el comando **exiftool cat.jpg** y obtenemos lo siguiente:

<img width="662" height="512" alt="Screenshot_20260712_211905" src="https://github.com/user-attachments/assets/94fd160f-2c16-4e9d-a76c-c1662ec852bf" />

En la parte de **License** vemos lo siguiente:

**cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9**

Decodificamos con cyberchef y obtenemos la flag:

**picoCTF{the_m3tadata_1s_modified}**

Subimos la flag a picoctf y listo.

<img width="1372" height="102" alt="Screenshot_20260712_212203" src="https://github.com/user-attachments/assets/f842fc95-163c-4d85-b38d-336a08982954" />
