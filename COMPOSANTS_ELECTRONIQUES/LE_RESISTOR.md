# LES RÉSISTORS

<table>
  <tr>
    <td align="center" valign="top">
      <img src="https://github.com/user-attachments/assets/dc06499b-0a59-4f97-9c17-fda84f032185" alt="résistor" width="323" height="238" />
    </td>
    <td align="center" valign="top">
      <img width="945" height="475" alt="5190177" src="https://github.com/user-attachments/assets/d435db39-98a0-4c48-b955-ea01a857ba2c" />
    </td>
  </tr>
</table>

## A) QU'EST-CE QU'UN RÉSISTOR ?

## 1. Définition
C'est un composant électronique dipôle passif dont la caractéristique physique est la résistance.

---

## 2. Rôle dans un circuit
C'est un composant électrique qui réduit le passage du courant dans le circuit électrique ou qui fait chuter la tension.

---

## 3. Principe de fonctionnement
Il oppose des obstacles physiques au passage des électrons, lesquels entrent en collision continue avec ses atomes, ce qui freine leur déplacement et limite ainsi l'intensité du courant électrique.

Lors de ces chocs, les électrons transfèrent leur énergie cinétique aux atomes, provoquant une agitation atomique qui se traduit par un dégagement de chaleur (l'effet Joule).

> **NB :** 
> - **L'effet Joule :** C'est la transformation de l'énergie électrique en énergie thermique lorsqu'un courant traverse un matériau conducteur ou résistant.
> - **Haute fréquence :** En haute fréquence, le résistor subit des effets parasites (inductances et capacités parasites) liés à sa géométrie.

---

## 4. Les caractéristiques fondamentales

### a) La résistance
- C'est la mesure de sa capacité à s'opposer au passage du courant. 
  $$U = R \times I$$ (avec $U$ en volts, $R$ en ohms et $I$ en ampères).
- La courbe caractéristique du résistor est $I = f(U)$. C'est une droite linéaire passant par l'origine, dont la pente $\frac{1}{R}$ représente la conductance.

### b) La tolérance 
C'est la variation maximale possible (en pourcentage) entre la valeur réelle du résistor et sa valeur théorique lisible grâce au code couleur.

### c) La puissance maximale admissible
- Il possède une limite physique de puissance qu'il peut dissiper sans griller. 
  $$P = U \times I = R \times I^2$$ (avec $P$ en watts).
- Valeurs courantes : 0,25 W ; 0,5 W ; 1 W.

### d) La tension maximale d'utilisation ($U_{max}$)
C'est la tension de claquage. Si elle est dépassée, un arc électrique détruit le composant, indépendamment de la puissance maximale dissipée.

### e) Le coefficient de température (TCR) 
La valeur d'une résistance varie en fonction de sa température. Le TCR indique de combien la valeur ohmique dérive lorsque la température change.

$$R_T = R_0 \cdot (1 + \alpha \cdot \Delta T)$$

* $R_T$ : Résistance finale à la température $T$
* $R_0$ : Résistance initiale à la température de référence $T_0$
* $\alpha$ : Coefficient de température (TCR)
* $\Delta T$ : Écart de température ($T - T_0$)

> **NB :** 
> - **TCR positif :** La résistance augmente avec la température.
> - **TCR négatif :** La résistance diminue avec la température.

### f) L'association des résistors
- **En série :** $$R_{eq} = R_1 + R_2 + \dots + R_n$$
- **En parallèle :** $$\frac{1}{R_{eq}} = \sum_{i=1}^{n} \frac{1}{R_i}$$

---

# B) LES VARIANTES DU COMPOSANT

<table>
  <tr>
    <td align="center" valign="top">
      <img width="150" height="150" style="object-fit: cover;" alt="résistor classique" src="https://github.com/user-attachments/assets/e2cd65c9-e498-44cb-a10e-780c7851ef8e" />
    </td>
    <td align="center" valign="top">
      <img width="150" height="150" style="object-fit: cover;" alt="potentiomètre" src="https://github.com/user-attachments/assets/71793d55-d62a-4a2b-9823-b0bd82802404" />
    </td>
    <td align="center" valign="top">
<img width="150" height="150" style="object-fit: cover;" alt="trimmer" src="https://github.com/user-attachments/assets/2dfa307e-3686-49ae-a270-c8cfebfd434c" />
    </td>
    <td align="center" valign="top">
      <img width="150" height="150" style="object-fit: cover;" alt="photorésistance" src="https://github.com/user-attachments/assets/5863aa3d-3147-451d-84fd-732300347edc" />
    </td>
    <td align="center" valign="top">
      <img width="150" height="150" style="object-fit: cover;" alt="thermistance" src="https://github.com/user-attachments/assets/7ba963b2-34d3-42c9-96e6-b8bb74784fa1" />
    </td>
    <td align="center" valign="top">
      <img width="150" height="150" style="object-fit: cover;" alt="réseau de résistors" src="https://github.com/user-attachments/assets/5760284e-914c-444e-bb2f-bb416c478d5c" />
    </td>
  </tr>
  <tr>
    <td align="center">Le résistor fixe</td>
    <td align="center">Le potentiomètre</td>
    <td align="center">Le trimmer</td>
    <td align="center">La photorésistance (LDR)</td>
    <td align="center">La thermistance (NTC/PTC)</td>
    <td align="center">Le réseau de résistors SIL</td>
  </tr>
</table>

---

# C) MONTAGES ILLUSTRANT LES RÔLES DU RÉSISTOR 

## 1. Le rôle de protection (Limitation de courant)
<table>
  <tr>
    <td align="center" valign="middle">
      <img width="300" height="300" alt="Montage de protection DEL" src="https://github.com/user-attachments/assets/e9284fc4-4645-4020-92a7-eb5c7026611c" />
    </td>
    <td valign="middle" style="padding-left: 20px;">
      <h3>Composants du circuit :</h3>
      <ul>
        <li>1 Résistor de 220 $\Omega$</li>
        <li>1 DEL rouge</li>
        <li>1 Alimentation de 5 V</li>
      </ul>
    </td>
  </tr>
</table>

Dans ce montage, le résistor de 220 ohms est placé en série avec une DEL rouge (tension de seuil $U_{DEL} = 1,8\text{ V}$). L'alimentation délivre 5 V. Le résistor absorbe l'excès de tension et limite le courant pour protéger la DEL d'une destruction thermique instantanée.

D'après la loi des mailles et la loi d'Ohm, le courant qui circule dans ce circuit est de : 
$$I = \frac{U_{alim} - U_{DEL}}{R} \implies I = \frac{5 - 1,8}{220} \approx 14,5\text{ mA}$$

---

## 2. Le rôle de diviseur de tension (Adaptation de niveau)
<table>
  <tr>
    <td align="center" valign="middle">
      <img width="300" height="300" alt="Montage diviseur de tension" src="https://github.com/user-attachments/assets/f37b04d3-f30c-43d4-aa8b-304838e36eb4" />
    </td>
    <td valign="middle" style="padding-left: 20px;">
      <h3>Composants du circuit :</h3>
      <ul>
        <li>2 Résistors de 220 $\Omega$</li>
        <li>1 Alimentation de 5 V</li>
      </ul>
    </td>
  </tr>
</table>

Ici, les résistors servent à configurer un niveau de tension intermédiaire. Ce montage permet de diviser ou d'abaisser la tension d'entrée de 5 V pour obtenir une référence d'environ 2,5 V au point milieu. 

Formule mathématique du pont diviseur : 
$$U_{out} = U_{entrée} \times \frac{R_2}{R_1 + R_2}$$

### Mesure au multimètre
<table>
  <tr>
    <td align="center" valign="middle">
      <img width="300" height="400" alt="Mesure multimètre diviseur de tension" src="https://github.com/user-attachments/assets/0ee109a2-a90b-433d-862e-453c7a495404" />
    </td>
    <td valign="middle" style="padding-left: 20px;">
      Tension mesurée aux bornes du résistor $R_1$, confirmant le partage proportionnel de la tension d'alimentation.
    </td>
  </tr>
</table>

---

## 3. Le rôle de contrôle du signal (Résistances de Pull-Up / Pull-Down)
> **Note théorique de synthèse :**
> En électronique numérique (circuits logiques ou microcontrôleurs), les entrées sont extrêmement sensibles. Lorsqu'un bouton-poussoir est ouvert, la ligne de signal ne doit jamais rester déconnectée ou "flottante", sous peine de capter les parasites électromagnétiques environnants et de générer des états logiques instables (oscillations aléatoires entre 0 et 1).
> 
> Un résistor de forte valeur (généralement $10\text{ k}\Omega$) est alors utilisé pour imposer un état électrique par défaut propre et stable :
> - **Pull-Up :** Relie la ligne au +Vcc pour forcer un état HAUT (1 logique) par défaut.
> - **Pull-Down :** Relie la ligne au GND pour forcer un état BAS (0 logique) par défaut.

---

## 4. Le rôle de variation dynamique (Le potentiomètre)
<table>
  <tr>
    <td align="center" valign="middle">
      <img width="300" height="300" alt="Montage potentiomètre" src="https://github.com/user-attachments/assets/df653e45-675a-404c-921a-f32f1dcc7716" />
    </td>
    <td valign="middle" style="padding-left: 20px;">
      <h3>Composants du circuit :</h3>
      <ul>
        <li>1 Résistor de 220 $\Omega$</li>
        <li>1 DEL rouge</li>
        <li>1 Potentiomètre 3386P de 10 k$\Omega$</li>
        <li>1 Alimentation de 5 V</li>
      </ul>
    </td>
  </tr>
</table>

Dans ce montage, la molette du potentiomètre de 10 k$\Omega$ modifie manuellement la résistance totale de la branche. Cela fait varier la tension et l'intensité du courant aux bornes de la DEL (toujours protégée en série par le résistor de 220 $\Omega$), contrôlant ainsi dynamiquement sa luminosité.

### Mesures au multimètre selon la position du curseur

#### • Curseur à la résistance minimale ($R \approx 0\ \Omega$)
<table>
  <tr>
    <td align="center" valign="top">
      <img width="250" alt="Potentiomètre à 0k" src="https://github.com/user-attachments/assets/7779c0e8-36de-45f4-b289-299acffae770" />
    </td>
    <td align="center" valign="top">
      <img width="250" alt="Tension DEL à 0k" src="https://github.com/user-attachments/assets/2af3fc23-0935-4179-9f09-5904059011ef" />
    </td>
    <td align="center" valign="top">
      <img width="250" alt="Tension résistor à 0k" src="https://github.com/user-attachments/assets/789cdf8a-9830-44d9-9470-1380d0ad7fdc" />
    </td>
  </tr>
  <tr>
    <td align="center">Potentiomètre réglé à 0 $\Omega$</td>
    <td align="center">Tension DEL</td>
    <td align="center">Tension résistor</td>
  </tr>
</table>

#### • Curseur à la résistance maximale ($R \approx 10\text{ k}\Omega$)
<table>
  <tr>
    <td align="center" valign="top">
      <img width="250" alt="Potentiomètre à 10k" src="https://github.com/user-attachments/assets/e040678f-62f1-4c50-a175-273158acd81b" />
    </td>
    <td align="center" valign="top">
      <img width="250" alt="Tension DEL à 10k" src="https://github.com/user-attachments/assets/e485d7fb-ec07-4bf6-86bd-66a279d94bdf" />
    </td>
    <td align="center" valign="top">
      <img width="250" alt="Tension résistor à 10k" src="https://github.com/user-attachments/assets/9b090064-4f0c-4e6f-abd4-9be7dc7d1be3" />
    </td>
  </tr>
  <tr>
    <td align="center">Potentiomètre réglé à 10 k$\Omega$</td>
    <td align="center">Tension DEL</td>
    <td align="center">Tension résistor</td>
  </tr>
</table>

## 4. Le rôle de variation dynamique (Le potentiomètre)
<table>
  <tr>
    <td align="center" valign="middle">
      <img width="300" height="300" alt="Montage potentiomètre" src="https://github.com/user-attachments/assets/df653e45-675a-404c-921a-f32f1dcc7716" />
    </td>
    <td valign="middle" style="padding-left: 20px;">
      <h3>Composants du circuit :</h3>
      <ul>
        <li>1 Résistor de 220 $\Omega$</li>
        <li>1 DEL rouge</li>
        <li>1 Potentiomètre 3386P de 10 k $\Omega$</li>
        <li>1 Alimentation de 5 V</li>
      </ul>
    </td>
  </tr>
</table>

Dans ce montage, la molette du potentiomètre de 10 k $\Omega$ modifie manuellement la résistance totale de la branche. Cela fait varier la tension et l'intensité du courant aux bornes de la DEL (toujours protégée en série par le résistor de 220 $\Omega$), contrôlant ainsi dynamiquement sa luminosité.

### Mesures au multimètre selon la position du curseur
#### • Curseur à la résistance maximale ($R \approx 10\text{ k }\Omega$)
<table>
  <tr>
    <td align="center" valign="top">
      <img width="250" alt="Potentiomètre à 10k" src="https://github.com/user-attachments/assets/e040678f-62f1-4c50-a175-273158acd81b" />
    </td>
    <td align="center" valign="top">
      <img width="250" alt="Tension DEL à 10k" src="https://github.com/user-attachments/assets/e485d7fb-ec07-4bf6-86bd-66a279d94bdf" />
    </td>
    <td align="center" valign="top">
      <img width="250" alt="Tension résistor à 10k" src="https://github.com/user-attachments/assets/9b090064-4f0c-4e6f-abd4-9be7dc7d1be3" />
    </td>
  </tr>
  <tr>
    <td align="center">Potentiomètre réglé à 10 k $\Omega$</td>
    <td align="center">Tension DEL</td>
    <td align="center">Tension résistor</td>
  </tr>
</table>
