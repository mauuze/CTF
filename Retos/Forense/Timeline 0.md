# Timeline 0

**Can you find the flag in this disk image? Wrap what you find in the picoCTF flag format.**

Todas los comandos utilizados son de la herramienta sleuthkit.

Primero obtenemos la informacion de los archivos que se encuentran en el archivo **partition4.img** con el comando:

**fls -m / -r partition4.img > bodyfile.txt**

Luego generamos una linea de tiempo ordenada cronologicamente con el comando:

**mactime -b bodyfile.txt > timeline.txt**

Ahora procdemos a observar el contenido del archivo timeline que se ve asi:

<img width="749" height="702" alt="Screenshot_20260712_221005" src="https://github.com/user-attachments/assets/c1dfa155-bb9f-4162-9cfa-da90f5cf4fa6" />

Como tenemos la pista **Sloppy timestomping can yield strange (very old) timestamps** procedemos a ver los archivos mas antiguos, el mas antiguo correnponde al id de archivo 4945, con el cisguiente comando:

**icat partition41.img 4945**

Donde obtenemos lo siguiente:

**NzFtMzExbjNfMHU3MTEzcl9oM3JfNDNhMmU3YWY**

Si lo decodificamos nos da:

**71m311n3_0u7113r_h3r_43a2e7af**

Que corresponde a la parte de las llaves de picoCTF{}, por lo tanto la flag es:

**picoCTF{71m311n3_0u7113r_h3r_43a2e7af}**

Subimos la flag a picoctf y listo.

<img width="1376" height="94" alt="Screenshot_20260712_221802" src="https://github.com/user-attachments/assets/85eee05f-4afb-4961-ab38-ed086f3fdaf8" />
