# Rogue Tower
**A suspicious cell tower has been detected in the network. Analyze the captured network traffic to identify the rogue tower, find the compromised device, and recover the exfiltrated flag.**

Primero vemos el puerto UDP 55000 y obtenemos algo interesante que es lo siguiente:

**UNAUTHORIZED-TEST-NETWORK PLMN=00101 CELLID=92058**

Ahora pocedemos a ver los HTTP User-Agent headers pero buscando con el CELLID que ya encontramos y obtenemos lo siguiente:

**User-Agent: MobileDevice/1.0 (IMSI:310410308555787; CELL:92058)**

Esta parte es importante ya que tenemos una pista que nos dice **The encryption key is derived from the victim device's IMSI**.

Ahora vemos los HTTP POST requests y en cada parte de ellos vemos una fraccion de una codigo:

**QFFWWnZjf**

**kxCCFJABm**

**hbBFxUakE**

**FQAtFb1xX**

**VgEHAAQBR**

**Q==**

Decoficando el codigo con cyberchef, Base64, se obtenia lo siguiente:

**@QVZvc~LBR@h[\TjA@Eo\WV**

Que no tenia nada que ver con una flag, como el problemas nos dice que la IMSI tiene la clave lo mas probable es que esto se trate de un cifrado XOR ademas del Base64 pero al utilizar esos 2 juntos se obtenia lo siguiente:

**qUFjó6KsBp=#mPzqsB^XGfRx0A**

Que de igual manera no tenia nada que ver con una flag, analizando un poco mas otra IMSI, **IMSI:310410316992912**, se puede observar que se repiten los numeros **3104103** por lo que estos probablemente esos sean la key correcta pero al probarlos seguian sin dar la flag por lo que decidi probar los otro numeros que no se repetian  que son **08555787** y ya con estos numeros como key obtenemos la flag:

**picoCTF{r0gu3_c3ll_t0w3r_dbc40831}**

Subimos la flag a picoctf y listo.

<img width="1372" height="89" alt="Screenshot_20260712_230845" src="https://github.com/user-attachments/assets/2019b204-9c76-4571-a287-4afab7d1c48e" />
