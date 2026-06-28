# Old Sessions

**Proper session timeout controls are critical for securing user accounts. If a user logs in on a public or shared computer but doesn’t explicitly log out (instead simply closing the browser tab), and session expiration dates are misconfigured, the session may remain active indefinitely.**

**This then allows an attacker using the same browser later to access the user’s account without needing credentials, exploiting the fact that sessions never expire and remain authenticated.**

**Your friend tells you to check out a new social media platform he built a few years ago. Although its still under development, he said the site is almost complete. He also mentioned that he hates constantly logging into sites, and so has made his page that 'once you login, you never have to log-out again'!**

Al iniciar el reto nos encontramos en la pagina inicial de la web proporcionada, debemos crearnos una cuenta, al ingresar con la cuenta se puede notar un comentario que nos indica una pista, el comentario es el siguiente:

<img width="576" height="74" alt="image" src="https://github.com/user-attachments/assets/c0e39fa7-4c0f-4c6c-8568-10a2f0a019d6" />

Una vez entramos a la paginas:

**http://dolphin-cove.picoctf.net:52686/sessions**

nos cencontramos lo siguiente:

<img width="726" height="76" alt="image" src="https://github.com/user-attachments/assets/b2ecebaf-c4d7-4f2d-bed9-c4011aa0b91f" />

Esas son las cookies de inicio de sesion de usuario, ya que en el propio reto nos indica que estas nunca se borran, ingresamos a la parte de inspeccionar en el ordenador y nos dirigimos a las cookies del sitio y cambiomos la nuestra que es **OyxyjjPyFp3CMI_1FirQCdDa5vA4y2ljq9FVBbjNdMw** por la de admin que es **B8guXdi2qnd9GT53EKUUSiUcwayM4q2IqBO8fzLnobU**

<img width="943" height="765" alt="image" src="https://github.com/user-attachments/assets/d026ffa6-e88d-4a30-b80d-f5330e9a5a36" />


una vez ya cambiada volvemos a la pagina principal donde ahora nos encontramos con la flag:

**picoCTF{s3t_s3ss10n_3xp1rat10n5_77b6684a}**

Subimos la flag a picoctf y listo.

<img width="775" height="113" alt="image" src="https://github.com/user-attachments/assets/ec8561c1-6504-403e-945b-89c6bd5a45b0" />

