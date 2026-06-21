# Ph4nt0m 1ntrud3r

**A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag.**

**To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder!**

Se nos proporciona un archivo pcap, abrimos el archivo con Wireshark y podemos ver toda la lista de paquetes, si hacemos click derecho en TCP segment data y luego presionamos mostrar bytes  de paquete

<img width="1366" height="725" alt="Screenshot_20260621_184651" src="https://github.com/user-attachments/assets/39fb75d0-96b0-43c5-9432-1a66707808e9" />

Obtenemos un codigo en Base64:

**cGljboNURg==**

Si llevamos ese codigo a cyberchef obtenemos lo siguiente:

**picoCTF**

Esta es la parte inicial de nuestra flag. Si seguimos analizando los paquetes obtenemos los siguientes codigos en Base64:

**cGljb0NURg==**
**ezF0X3c0cw==**
**bnRfdGg0dA==**
**XzM0c3lfdA==**
**YmhfNHJfOQ==**
**NTlmNTBkMw==**
**fQ==**

Si llevamos todo esto a cyberchef obtenemos la flag:

**picoCTF{1t_w4snt_th4t_34sy_tbh_4r_959f50d3}**

Subimos la flag a picoctf y listo.

<img width="995" height="124" alt="Screenshot_20260621_190216" src="https://github.com/user-attachments/assets/b26fbb79-984c-4463-8124-032a313529f0" />
