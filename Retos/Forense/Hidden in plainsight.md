# Hidden in plainsight
**You’re given a seemingly ordinary JPG image. Something is tucked away out of sight inside the file. Your task is to discover the hidden payload and extract the flag.**

Descargamos la imagen del reto y vemos los metadatos de esta, ahí encontramos lo siguiente:

**c3RlZ2hpZGU6Y0VGNmVuZHZjbVE9**

Con la ayuda de cyberchef lo decodificamos y nos da lo siguiente:

**steghide:cEF6endvcmQ=**

Ahora solo decodificamos la parte de **cEF6endvcmQ=** y obtenemos:

**pAzzword**

Por lo que todo completo seria:

**steghide:pAzzword**

Esto es una pista de la siguiente herramienta a utilizar que es **steghide**. Steghide es una herramienta que permite ocultar archivos o mensajes secretos dentro de otros archivos ordinarios (como imágenes o audios) sin alterar su apariencia externa y también permite extraer esos archivos ocultos.

Utilizamos el comando steghide img.jpg para ver si la imagen contiene algún archivo oculto, luego de ingresar el comando nos pide una contraseña introducimos **pAzzword** y podemos observar que existe un archivo adjunto llamado flag.txt

<img width="859" height="224" alt="image" src="https://github.com/user-attachments/assets/72a80be0-cd37-4c8d-b794-2b3559efb7a1" />

Para extraer el archivo utilizamos el comando:

**steghide extract -sf img.jpg**

<img width="628" height="87" alt="image" src="https://github.com/user-attachments/assets/48e6d351-a2dd-4d57-8b3f-253153b7887e" />


Observavmos el contenido del archivo flag.txt y obtenemos la flag:

**picoCTF{h1dd3n_1n_1m4g3_871ba555}**

Subimos la flag a picoctf y listo.

<img width="761" height="82" alt="image" src="https://github.com/user-attachments/assets/326af9a6-5410-4afe-af5a-828ce3369386" />
