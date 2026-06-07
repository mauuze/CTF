# Riddle Registry
**Hi, intrepid investigator! 📄🔍 You've stumbled upon a peculiar PDF filled with what seems like nothing more than garbled nonsense. But beware! Not everything is as it appears. Amidst the chaos lies a hidden treasure—an elusive flag waiting to be uncovered.**

A primera vista se intentaría buscar la flag en los textos tachados del pdf pero si los logras sacar son puro texto que no aporta nada como:

**Aenean lacinia bibendum nulla sed consectetur.**

o como:

**The author have done a great and good job**

Luego de ver los textos del pdf fui a ver los metadatos y en el autor se puede encontrar lo siguiente:

**cGljb0NURntwdXp6bDNkX20zdGFkYXRhX2YwdW5kIV8wZTJkZTVhMX0=**

Decodificamos ese codigo en Base64 con la herramienta cyberchef y obtenemos la flag:

**picoCTF{puzzl3d_m3tadata_f0und!_0e2de5a1}**

La subimos a picoctf y listo.

<img width="761" height="95" alt="Captura de pantalla 2026-06-07 023955" src="https://github.com/user-attachments/assets/baf1472e-416b-4593-8876-f125b907c5d0" />
