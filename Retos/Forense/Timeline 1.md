# Timeline 1

**Can you find the flag in this disk image? Wrap what you find in the picoCTF flag format.**

Primero obtenemos la informacion de los archivos que se encuentran en el archivo partition4.img con el comando:

**fls -m / -r partition4.img > body.txt**

Ahora creamos la linea de tiempo de los archivos con el comando:

**mactime -b body.txt > linea.tx**

Para buscar bien el archivo deseado tenemos la pista **Filter only new files by grepping for macb**, por lo que haremos un filtrado de solo esos archivos con el comando:

**more linea.txt | grep macb**

Obtendremos lo siguiente:

<img width="746" height="528" alt="Screenshot_20260712_223830" src="https://github.com/user-attachments/assets/8df2b02f-ff2a-4510-ac34-45bb29f0355e" />

Como tenemos la pista **Look at recent timestamps** procedemos a ver los archivos mas reciuentes y encontramos lo siguiente en el archivo con id **32716**:

**NTczNDE3aDEzcl83aDRuXzdoM18xNDU3XzU4NTI3YmIyMjIK**

Lo decodificamos y obtenemos lo siguiente:

**573417h13r_7h4n_7h3_1457_58527bb222**

Le agregamos la parte de picoCTF y obtenemos la flag:

**picoCTF{573417h13r_7h4n_7h3_1457_58527bb222}**

Subimos la flag a picoctf y listo.

<img width="1375" height="99" alt="Screenshot_20260712_224318" src="https://github.com/user-attachments/assets/452acc92-44ce-4e12-a4a0-79fe65cb6a4f" />
