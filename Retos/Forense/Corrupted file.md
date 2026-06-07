# Corrupted file
**This file seems broken... or is it? Maybe a couple of bytes could make all the difference. Can you figure out how to bring it back to life?**

Revisando el archivo parecia una imagen codificada por un fragmento en que nos dice **JFIF** pero al momento de usar la herramienta de Render Image de cyberchef esta fallaba y no entregaba nada, investigando un poco se puede encontrar que efectivamente es una imagen pero tiene las cabeceras corruptas como ya nos menciona el enunciado.

Las cabeceras hexadecimales o los primeros bytes correctos de una imagen por lo general son:

**FF D8 FF E0**

Con un herramienta llamada hexed obtenemos que las cabeceras del archivo corrupto son:

**5C 78 FF E0**

<img width="584" height="295" alt="image" src="https://github.com/user-attachments/assets/a8f35199-8b61-4fc8-940c-11e6d5e448ed" />

Con la misma herramienta corregimos la cabecera a **FF D8 FF E0** y recién subimos la imagen a cyberchef donde ya obtenemos la flag:

<img width="272" height="109" alt="image" src="https://github.com/user-attachments/assets/486e0abd-e841-407f-979b-d82787a8b732" />


Subimos la flag a picoctf y listo.

<img width="761" height="87" alt="image" src="https://github.com/user-attachments/assets/bc7fd3b7-44bf-4145-9247-d666c8fb80fa" />
