# Flag in Flame
**The SOC team discovered a suspiciously large log file after a recent breach. When they opened it, they found an enormous block of encoded text instead of typical logs. Could there be something hidden within? Your mission is to inspect the resulting file and reveal the real purpose of it. The team is relying on your skills to uncover any concealed information within this unusual log.**

Subimos el archivo logs a cyberchef y utilizamos la decodificación FROM Base64 y Render Image de cyberchef, esto nos entrega la siguiente imagen:

<img width="896" height="1152" alt="download (1)" src="https://github.com/user-attachments/assets/bc31e6b2-0960-4192-affc-737b51986bc9" />

Extraemos el codigo de la imagen que es:

**7069636F4354467B666F72656E736963735F616E616C797369735F69735F616D617A696E675F65633139383466637D**

Decodificamos el codigo con un decodificar de hexadecimal y obtenemos la flag:

**picoCTF{forensics_analysis_is_amazing_ec1984fc}**

Subimos la flag a picoctf y listo.

<img width="770" height="85" alt="image" src="https://github.com/user-attachments/assets/40320189-cd62-457e-8b1f-261a78a5453d" />
