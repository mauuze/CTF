# Crack the Gate 1

**We’re in the middle of an investigation. One of our persons of interest, ctf player, is believed to be hiding sensitive data inside a restricted web portal. We’ve uncovered the email address he uses to log in: ctf-player@picoctf.org. Unfortunately, we don’t know the password, and the usual guessing techniques haven’t worked. But something feels off... it’s almost like the developer left a secret way in. Can you figure it out?**

Revisando el codigo de la pagina con la opción de inspeccionar nos encontramos con lo siguiente:

**<!-- ABGR: Wnpx - grzcbenel olcnff: hfr urnqre "K-Qri-Npprff: lrf" -->**
**<!-- Remove before pushing to production! -->**

Que si decodificamos nos da lo siguiente:

**NOTE: Jack - temporary bypass: use header "X-Dev-Access: yes"**

Utilizando la extensión para navegador ModHeader introducimos los que se nos proporciona:

<img width="624" height="510" alt="image" src="https://github.com/user-attachments/assets/cef12910-b64c-4916-b20d-324bf6dd3aae" />


Ahora si intentamos iniciar sesion con el correo que nos da el reto y ponemos cualquier contraseña se nos da la flag:

<img width="721" height="696" alt="image" src="https://github.com/user-attachments/assets/be0c8cfa-a6a9-4789-870d-db497d10fcd4" />

Que es la siguiente:

**picoCTF{brut4_f0rc4_3c6b118b}**

Subimos la flag a picoctf y listo.

<img width="770" height="116" alt="image" src="https://github.com/user-attachments/assets/a0c28f7c-b55e-47f3-9221-dfe9ff6566c2" />
