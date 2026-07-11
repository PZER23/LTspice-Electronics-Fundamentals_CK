# LES RESISTORS
<table>
  <!-- Ligne des images -->
  <tr>
    <td align="center" valign="top">
<img src="https://github.com/user-attachments/assets/dc06499b-0a59-4f97-9c17-fda84f032185" alt="résistor" width="323" height="238" />
    </td>
    <td align="center" valign="top">
      <img width="945" height="475" alt="5190177" src="https://github.com/user-attachments/assets/d435db39-98a0-4c48-b955-ea01a857ba2c" />
    </td>
  </tr>
</table>

## A) C'EST QUOI LE RESISTOR
## 1. Définition
C'est un composant électronique dipole passif dont la caracteristique physique est la resistance.

---

## 2. Rôle dans un circuit
C'est un composant électrique qui réduit le passage du courant dans le circuit electrique ou qui fait chuter la tension

---

## 3. Principe de fonctionnement
Il oppose des obstacles physiques au passage des électrons, lesquels entrent en collision continue avec ses atomes, ce qui freine leur déplacement et limite ainsi l'intensité du courant électrique.

Lors de ces chocs les électrons transfèrent lleur énergie cinétique aux atomes, provoquant une agitation atomique qui se traduit par un dégagement de chaleur (l'effet joule).

NB : 
- L'effet joule c'est la transformation de l'énergie électrique en énergie thermique lorsqu'un courant traverse un materiau conducteur ou resistant.
- En haute frequenece le resistor subit des effets parasites (inductances et capacite parasite).

---
## 4. Les caracteristiques fondamentales
### a) La resistance
- c'est la mesure de sa capacite a s'opposer au passage du courant. U = R x I (U en volt; Ren ohm, I en ampère)
- La courbe caracteristiquesdu resistor : I=f(U) ; la pente 1/R est la conductance.
- 
### b) La tolérance 
C'est la variation entre la valeur réelle du resistor et sa valeur théorique lisible grace au code couleur.

### c)La puissance maximale admissible
- Il possède une limite de puissance qu'il peut libérer sans griller. P = U x I en watt (W)
- Valeurs courates : 0.25 W; 0,5 W ; 1 W
### d) La tension maximale d'utilisation (Umax)
C'est la tension de claquage. Elle ne doit pas etre appliquer sur le resistor.

### e) Le coefficient de temperature (TCR) 
La valeur d'une resitance varie en fonction de sa temperature. Il indique de combien la resistance varie lorsque la temperature change.
NB : 
- TCR positif -> resitance augmente avec la temperature
- TCR negatif -> resistance diminu avec la temperature

$$R_T = R_0 \cdot (1 + \alpha \cdot \Delta T)$$

### L'association des resistors
- En serie $$R_{eq} = R_1 + R_2 + ...$$
- En paralelle $$\frac{1}{R_{eq}} = \sum_{i=1}^{n} \frac{1}{R_i}$$

---
# B) LES VARIANTES DU COMPOSANT
<table>
  <!-- Ligne des images -->
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
  <!-- Ligne des noms -->
  <tr>
    <td align="center">Le résitor</td>
    <td align="center">Le potentiomètre</td>
    <td align="center">Le trimmer</td>
    <td align="center">La photorésistance</td>
    <td align="center">La thermistance</td>
    <td align="center">Les réseaux de résistors SIL</td>
  </tr>
</table>

---

# C) MONTAGES ILLUSTRANT LE ROLE DU RESISTOR 
# 1. Le role de protection
<table>
  <tr>
    <!-- Colonne de l'image -->
    <td align="center" valign="middle">
      <img width="300" height="300" alt="WhatsApp Image 2026-07-08 at 04 42 23" src="https://github.com/user-attachments/assets/e9284fc4-4645-4020-92a7-eb5c7026611c" />
    </td>
    <!-- Colonne du texte à côté -->
    <td valign="middle" style="padding-left: 20px;">
      <h3>Composants du circuit :</h3>
      <ul>
        <li>Résistance de 220 Ω</li>
        <li>Une DEL rouge</li>
        <li>Alimentation de 5 V</li>
      </ul>
    </td>
  </tr>
</table>

Dans ce montage le resistor est place en serie avec une DEL (tension seuil 1.8 v)
