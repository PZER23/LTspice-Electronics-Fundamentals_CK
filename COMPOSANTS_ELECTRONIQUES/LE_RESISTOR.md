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

NB : 
- L'effet Joule, c'est la transformation de l'énergie électrique en énergie thermique lorsqu'un courant traverse un matériau conducteur ou résistant.
- En haute fréquence, le résistor subit des effets parasites (inductances et capacités parasites).

---
## 4. Les caractéristiques fondamentales
### a) La résistance
- C'est la mesure de sa capacité à s'opposer au passage du courant. $U = R \times I$ (avec $U$ en volts, $R$ en ohms et $I$ en ampères).
- La courbe caractéristique du résistor : $I=f(U)$ ; la pente $\frac{1}{R}$ représente la conductance.

### b) La tolérance 
C'est la variation maximale possible entre la valeur réelle du résistor et sa valeur théorique lisible grâce au code couleur.

### c) La puissance maximale admissible
- Il possède une limite de puissance qu'il peut dissiper sans griller. $P = U \times I$ en watts (W).
- Valeurs courantes : 0,25 W ; 0,5 W ; 1 W.

### d) La tension maximale d'utilisation ($U_{max}$)
C'est la tension de claquage. Elle ne doit pas être appliquée sur le résistor sous peine de le détruire.

### e) Le coefficient de température (TCR) 
La valeur d'une résistance varie en fonction de sa température. Il indique de combien la résistance varie lorsque la température change.

NB : 
- TCR positif -> la résistance augmente avec la température.
- TCR négatif -> la résistance diminue avec la température.

$$R_T = R_0 \cdot (1 + \alpha \cdot \Delta T)$$

### f) L'association des résistors
- En série : $$R_{eq} = R_1 + R_2 + \dots$$
- En parallèle : $$\frac{1}{R_{eq}} = \sum_{i=1}^{n} \frac{1}{R_i}$$

---
# B) LES VARIANTES DU COMPOSANT
<table>
  <tr>
    <td align="center" valign="top">
      <img width="150" height="150" style="object-fit: cover;" alt="images" src="https://github.com/user-attachments/assets/e2cd65c9-e498-44cb-a10e-780c7851ef8e" />
    </td>
    <td align="center" valign="top">
      <img width="150" height="150" style="object-fit: cover;" alt="images" src="https://github.com/user-attachments/assets/71793d55-d62a-4a2b-9823-b0bd82802404" />
    </td>
    <td align="center" valign="top">
      <img width="150" height="150" style="object-fit: cover;" alt="images" src="https://github.com/user-attachments/assets/9fa71185-5737-40cb-b4df-91c8fa396bbd" />
    </td>
    <td align="center" valign="top">
      <img width="150" height="150" style="object-fit: cover;" alt="images" src="https://github.com/user-attachments/assets/5863aa3d-3147-451d-84fd-732300347edc" />
    </td>
    <td align="center" valign="top">
      <img width="150" height="150" style="object-fit: cover;" alt="images" src="https://github.com/user-attachments/assets/7ba963b2-34d3-42c9-96e6-b8bb74784fa1" />
    </td>
    <td align="center" valign="top">
      <img width="150" height="150" style="object-fit: cover;" alt="images" src="https://github.com/user-attachments/assets/5760284e-914c-444e-bb2f-bb416c478d5c" />
    </td>
  </tr>
  <tr>
    <td align="center">Le résistor</td>
    <td align="center">Le potentiomètre</td>
    <td align="center">Le trimmer</td>
    <td align="center">La photorésistance</td>
    <td align="center">La thermistance</td>
    <td align="center">Le réseau de résistors SIL</td>
  </tr>
</table>

---

# C) MONTAGES ILLUSTRANT LE RÔLE DU RÉSISTOR 
## 1. Le rôle de protection
<table>
  <tr>
    <td align="center" valign="middle">
      <img width="300" height="300" alt="WhatsApp Image 2026-07-08 at 04 42 23" src="https://github.com/user-attachments/assets/e9284fc4-4645-4020-92a7-eb5c7026611c" />
    </td>
    <td valign="middle" style="padding-left: 20px;">
      <h3>Composants du circuit :</h3>
      <ul>
        <li>Résistance de 220 $\Omega$</li>
        <li>Une DEL rouge</li>
        <li>Alimentation de 5 V</li>
      </ul>
    </td>
  </tr>
</table>

Dans ce montage, le résistor de 220 ohms est placé en série avec une DEL rouge (tension de seuil de 1,8 V). L'alimentation est de 5 V.

D'après la loi des mailles, le courant qui circule dans ce circuit est : 
$$I = \frac{U_{alim} - U_{DEL}}{R} \implies I = \frac{5 - 1,8}{220} \approx 14,5\text{ mA}$$
