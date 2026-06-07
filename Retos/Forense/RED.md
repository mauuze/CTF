# RED
**RED, RED, RED, RED**
Lo primero que hice fue revisar los metadatos de la imagen, al hacer esto encontramos una sección llamada poem que contiene lo siguiente:

**Crimson heart, vibrant and bold, Hearts flutter at your sight. Evenings glow softly red, Cherries burst with sweet life. Kisses linger with your warmth. Love deep as merlot. Scarlet leaves falling softly, Bold in every stroke.**

Al inicio parece un poema que solo habla acerca del color rojo, pero si alineamos cada letra mayuscula obtenemos lo siguiente:

**C**rimson heart, vibrant and bold,\
**H**earts flutter at your sight.\
**E**venings glow softly red,\
**C**herries burst with sweet life.\
**K**isses linger with your warmth.\
**L**ove deep as merlot.\
**S**carlet leaves falling softly,\
**B**old in every stroke.

El mensaje que obtenemos en **CHECKLSB** esto nos dice que busquemos en los Least Significant Bit que es el último bit de la cadena binaria que representa el color de un píxel.

Utilizamos la herramienta zsteg para inspeccionar los LSB con el comando:

**zsteg red.png**

y obtenemos lo siguiente:

<img width="1501" height="285" alt="image" src="https://github.com/user-attachments/assets/891dc4ff-7f1f-4634-85d7-5d2a4947d55d" />

Como se puede observar en la parte de b1,rgba,lsb,xy nos aparece un codigo en Base64, llevamos el codigo a cyberchef y obtenemos la flag:

**picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}**

Subimos la flag a picoctf y listo.

<img width="765" height="92" alt="image" src="https://github.com/user-attachments/assets/6bc64d8a-e20b-4280-9d59-bdce38b8b837" />
