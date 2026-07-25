# LES DIODES

## A) C'est quoi une diode ?

### 1. Définition
Une diode est un composant électronique semi-conducteur (un dipôle passif non linéaire) qui possède deux bornes asymétriques : l'**anode** (la borne positive) et la **cathode** (la borne négative, repérée par un anneau ou une bande de couleur sur le boîtier physique).

### 2. Rôle dans un circuit
Le rôle principal de la diode est d'agir comme une **valve ou un clapet anti-retour** pour le courant électrique. Elle autorise le passage du courant dans une seule direction (le sens passant) et le bloque complètement dans la direction opposée (le sens bloqué).

### 3. Principe de fonctionnement 

* **En polarisation directe (Sens passant) :** Tu branches le "+" de l'alimentation sur la zone P (Anode) et le "-" sur la zone N (Cathode). La force de la pile pousse les charges vers le centre, ce qui **écrase le mur**. Dès que la tension dépasse la taxe de passage minimale (tension de seuil de **0,7 V**), le mur s'effondre et les électrons circulent librement : le courant passe.
* **En polarisation inverse (Sens bloqué) :** Tu branches le "+" sur la zone N (Cathode) et le "-" sur la zone P (Anode). La pile aspiration les charges vers l'extérieur du composant, loin de la frontière. Résultat : **le mur s'élargit** et devient de plus en plus épais. Le courant est totalement bloqué.

### 4. Caractéristiques fondamentales
* **a) La tension de seuil ($V_f$ ou Forward Voltage) :** C'est la tension minimale nécessaire pour écraser le mur isolant en sens passant. Pour le silicium standard, elle est d'environ **0,6 V** à **0,7 V**.
* **b) Le courant direct maximal ($I_{f_{max}}$) :** L'intensité maximale que la diode peut laisser passer en continu sans surchauffer et brûler.
* **c) La tension inverse de claquage ($V_{br}$ ou Peak Inverse Voltage) :** La tension maximale que le mur peut bloquer à l'envers. Si on dépasse cette limite, le "barrage" explose (effet d'avalanche) et la diode est détruite par le courant qui s'engouffre à l'envers.
* **d) Le courant de fuite inverse ($I_r$) :** Le courant microscopique (quelques microampères) qui réussit à traverser le mur même quand la diode est bloquée.

---

## B) Les variantes du composant

Voici les variantes incontournables au format "traversant" (Through-Hole), faciles à commander et à utiliser sur plaque d'essai :

<table>
  <tr>
    <td align="center" valign="top">
      <img width="150" height="150" alt="1N4007-Rectifier-Diode-1000V-1A" src="https://github.com/user-attachments/assets/04cb019a-2fdf-4786-b898-031b7b550b16" />
    </td>
    <td align="center" valign="top">
      <img width="150" height="150" alt="1N4148" src="https://github.com/user-attachments/assets/52d34ce5-2f79-47e2-b70b-d1277adc6749" />
    </td>
    <td align="center" valign="top">
      <img width="150" height="150" alt="LED" src="https://github.com/user-attachments/assets/884ed201-1995-4f0c-93e2-1e812f713b88" />
    </td>
    <td align="center" valign="top">
      <img width="150" height="150" alt="Diode_shotsky" src="https://github.com/user-attachments/assets/4d51f48c-3484-4a8b-8496-2dcb4417a1f6" />
    </td>
    <td align="center" valign="top">
      <img width="150" height="150" alt="bzx85c-zener-diode-250x250" src="https://github.com/user-attachments/assets/54ad145d-5715-4542-8228-2156c3cfd17c" />
    </td>
  </tr>
  <tr>
    <td align="center">1N4007</td>
    <td align="center">1N4148</td>
    <td align="center">LED</td>
    <td align="center">1N5819</td>
    <td align="center">BZX55C</td>
  </tr>
</table>

* **1. La diode de redressement standard (ex : 1N4007) :** Le gros bras. Petit cylindre noir avec une bague grise. Elle encaisse de forts courants (jusqu'à **1 A**) et de hautes tensions (jusqu'à **1000 V**). Parfaite pour bloquer une inversion de polarité.
* **2. La diode de petit signal (ex : 1N4148) :** Le sprinter. Tout petit boîtier en verre orange avec une bague noire. Elle ne supporte pas les gros courants (max **300 mA**) mais elle s'ouvre et se ferme à toute vitesse. Idéale pour les signaux logiques et les hautes fréquences.
* **3. La LED (Diode Électroluminescente) :** La star des indicateurs. Une diode optimisée pour convertir l'énergie électrique en lumière lorsqu'elle est traversée par un courant dans le sens passant.
* **4. La diode Schottky (ex : 1N5819) :** L'économe. Très rapide, elle possède surtout une tension de seuil minuscule (autour de **0,2 V** à **0,3 V**). Très utile dans les circuits à piles pour éviter de gaspiller de l'énergie.
* **5. La diode Zener (ex : série BZX55C) :** La soupape de sécurité. Contrairement aux autres, on l'utilisation volontairement *à l'envers* (en polarisation inverse). 

Au lieu d'être un barrage en béton qui explose si la tension inverse est trop forte, la Zener est fabriquée pour s'ouvrir proprement à une "pression" (tension) très précise fixée par le fabricant (par exemple **5,1 V**). Si la tension inversée atteint **5,1 V**, la soupape s'ouvre et laisse passer le surplus de courant à l'envers pour forcer la tension à rester bloquée à exactement **5,1 V**. On l'utilise pour réguler et stabiliser les tensions.

* **Un inconvénient à surveiller :** Si tu alimentes un montage avec une pile de 5 V et que tu mets cette diode pour protéger ton circuit, tes composants fragiles (comme un microcontrôleur Arduino ou un capteur) ne recevront que 4,3 V. Parfois, cette tension est trop faible pour qu'ils fonctionnent correctement. C'est pour cela qu'on utilise parfois des diodes Schottky, dont la taxe n'est que de 0,2 V.
* **Un avantage utile :** Comme cette chute de tension de 0,7 V est très stable, elle permet parfois de faire baisser volontairement et précisément une tension trop élevée dans un petit montage sans avoir à faire de calculs complexes.

---

## C) Montages illustrant le rôle de la diode

### Montage 1 : La protection du circuit (Le clapet anti-retour)
<table>
  <tr>
    <td align="center" valign="middle">
      <img width="300" height="400" alt="Montage Protection 1" src="https://github.com/user-attachments/assets/adbca42e-fe26-4f75-b83f-a52ff9d9edc5" /> 
    </td>
    <td valign="middle" style="padding-left: 20px;">
      <h3>Composants du circuit :</h3>
      <ul>
        <li>1 diode 1N4007</li>
        <li>1 résistor de 220 $\Omega$</li>
        <li>1 DEL rouge</li>
        <li>1 alimentation de 5 V</li>
      </ul>
    </td>
  </tr>
</table>

* **Le circuit :** Alimentation **5 V** $\rightarrow$ Diode 1N4007 (Anode côté 5V, Cathode côté circuit) $\rightarrow$ LED $\rightarrow$ Résistance de **220\ $\Omega$** $\rightarrow$ GND.
* **L'expérience :** 
  1. Dans ce sens (polarisation directe), le courant circule et la LED s'allume. 
  2. Si on retourne la diode sur la breadboard (Cathode côté 5V), elle passe en polarisation inverse, bloque tout et la LED reste éteinte.
* **Conclusion :** Placer cette diode à l'entrée du montage permet de faire barrage au courant si la pile est branchée à l'envers par erreur, sauvant ainsi tes composants fragiles.

## Calcul théorique en polarisation directe
$U_{\text{entrée}} = 5\text{ V}$ , $U_{\text{1N4007}} = 0,7\text{ V}$, $U_{\text{LED}} = 1,8\text{ V}$. Calculons $U_{\text{résistor}}$

On a : 
$$U_{\text{entrée}} = U_{\text{1N4007}} + U_{\text{LED}} + U_{\text{résistor}}$$
$$\rightarrow U_{\text{résistor}} = U_{\text{entrée}} - U_{\text{1N4007}} - U_{\text{LED}}$$
$$\rightarrow U_{\text{résistor}} = 5\text{ V} - 0,7\text{ V} - 1,8\text{ V}$$
$$\rightarrow U_{\text{résistor}} = 2,5\text{ V}$$

## Mesure des tensions en polarisation directe
<table>
  <tr>
    <td align="center" valign="top">
      <img width="170" height="170" alt="Mesure Diode Directe" src="https://github.com/user-attachments/assets/9bcefd23-a3d8-4978-a70e-16a4ae98ef53" />
    </td>
    <td align="center" valign="top">
      <img width="170" height="170" alt="Mesure LED Directe" src="https://github.com/user-attachments/assets/219d9b07-a675-41b2-b9e0-6cc13192f1d7" />
    </td>
    <td align="center" valign="top">
      <img width="170" height="170" alt="Mesure Resistor Directe" src="https://github.com/user-attachments/assets/b4a26318-890c-444e-aee6-945c72797ed5" />
    </td>
  </tr>
  <tr>
    <td align="center">tension diode</td>
    <td align="center">tension LED</td>
    <td align="center">tension résistor</td>
  </tr>
</table>

## Calcul théorique en polarisation inverse
$U_{\text{entrée}} = 5\text{ V}$ , $U_{\text{1N4007}} = 5\text{ V}$, $U_{\text{LED}} = 0\text{ V}$ , $U_{\text{résistor}} = 0\text{ V}$

## Mesure des tensions en polarisation inverse
<table>
  <tr>
    <td align="center" valign="top">
      <img width="170" height="170" alt="Mesure Diode Inverse" src="https://github.com/user-attachments/assets/43478787-4ed3-4c18-96c2-fb08d4be9be4" />
    </td>
    <td align="center" valign="top">
      <img width="170" height="170" alt="Mesure LED Inverse" src="https://github.com/user-attachments/assets/8408b9e4-243c-4f8b-86d0-ed20c262868f" />
    </td>
    <td align="center" valign="top">
      <img width="170" height="170" alt="Mesure Resistor Inverse" src="https://github.com/user-attachments/assets/d92d9f48-6735-4f41-bc59-1a4533d38d23" />
    </td>
  </tr>
  <tr>
    <td align="center">tension diode</td>
    <td align="center">tension LED</td>
    <td align="center">tension résistor</td>
  </tr>
</table>   

---

### Montage 2 : La chute de tension (La taxe de passage)

<table>
  <tr>
    <td align="center" valign="middle">
      <img width="300" height="400" alt="Montage Chute Tension 1" src="https://github.com/user-attachments/assets/6e0213c9-6d1b-49ef-9a67-b729837a714b" />
    </td>
    <td align="center" valign="middle">
      <img width="300" height="400" alt="Montage Chute Tension 2" src="https://github.com/user-attachments/assets/6885e4ec-0173-44ce-afcf-c53f8f43e8d0" />
    </td>
    <td valign="middle" style="padding-left: 20px;">
      <h3>Composants du circuit :</h3>
      <ul>
        <li>1 diode 1N4007</li>
        <li>1 résistor de 1 k $\Omega$</li>
        <li>1 alimentation de 5 V</li>
      </ul>
    </td>
  </tr>
</table>

* **Le circuit :** Alimentation **5 V** $\rightarrow$ Diode 1N4007 $\rightarrow$ Résistance de **1 k $\Omega$** $\rightarrow$ GND.
* **L'expérience :** La tension aux bornes de la diode est d'environ **0,7 V**. La tension aux bornes de la résistance sera d'environ **4,3 V**.
  $$V_{\text{alim}} - V_{\text{diode}} = V_{\text{résistance}}$$
  
* **Conclusion :** La diode consomme en permanence sa tension de seuil.
  
## Mesure des tensions
<table>
  <tr>
    <td align="center" valign="top">
      <img width="170" height="170" alt="Mesure Tension Diode M2" src="https://github.com/user-attachments/assets/0c06681d-5202-4394-ab5c-8c4a90c5a062" />
    </td>
    <td align="center" valign="top">
      <img width="170" height="170" alt="Mesure Tension Resistor M2" src="https://github.com/user-attachments/assets/d6a047ad-dd30-4d84-94f3-b6877cd20e6e" />
    </td>
  </tr>
  <tr>
    <td align="center">tension diode</td>
    <td align="center">tension résistor</td>
  </tr>
</table>

---
  
### Montage 3 : L'aiguillage logique 

<table>
  <tr>
    <td align="center" valign="middle">
      <img width="300" height="400" alt="Montage Aiguillage Logique" src="https://github.com/user-attachments/assets/4ed95388-47e8-46e0-babd-4beec6781862" />
    </td>
    <td valign="middle" style="padding-left: 20px;">
      <h3>Composants du circuit :</h3>
      <ul>
        <li>2 diodes 1N4007</li>
        <li>1 résistor de 220 $\Omega$</li>
        <li>1 LED ROUGE</li>
        <li>1 alimentation de 5 V</li>
      </ul>
    </td>
  </tr>
</table>

## Calcul théorique
$U_{\text{entrée}} = 5\text{ V}$, $U_{\text{LED}} = 1,8\text{ V}$. Calculons $U_{\text{résistor}}$, $U_{\text{D1}}$, $U_{\text{D2}}$
<table>
  <tr>
    <td align="center" valign="top">
      <img width="1361" height="888" alt="Schéma Aiguillage Logique" src="https://github.com/user-attachments/assets/da463e17-49d9-451e-8823-b55644263795" />
    </td>
  </tr>
</table>

#### 1. Calcul de la tension aux bornes du résistor ($V_{\text{R}}$) :
Selon la loi des mailles, la somme des tensions dans une boucle fermée est nulle :
$$V_{\text{cc}} - V_{\text{D}} - V_{\text{R}} - V_{\text{LED}} = 0$$

En isolant $V_{\text{R}}$ :
$$V_{\text{R}} = V_{\text{cc}} - V_{\text{D}} - V_{\text{LED}}$$
$$V_{\text{R}} = 5,0\text{ V} - 0,7\text{ V} - 2,0\text{ V} = 2,3\text{ V}$$

#### 2. Calcul de l'intensité théorique ($I_{\text{théorique}}$) :
En appliquant la Loi d'Ohm ($I = \frac{U}{R}$) au résistor :
$$I_{\text{théorique}} = \frac{V_{\text{R}}}{R}$$
$$I_{\text{théorique}} = \frac{2,3\text{ V}}{220\ \Omega} \approx 0,01045\text{ A}$$
$$I_{\text{théorique}} \approx 10,45\text{ mA}$$

#### 3. État et Tension de la Diode $D_2$ (Source $3,0\text{ V}$)

Pour comprendre l'isolation des sources, analysons la tension aux bornes de la diode $D_2$, connectée à la source secondaire de $3,0\text{ V}$.

La diode $D_1$ étant conductrice, elle fixe le potentiel du nœud commun (les cathodes reliées) à :
$$V_{\text{cathode}} = V_{\text{cc1}} - V_{\text{D1}} = 5,0\text{ V} - 0,7\text{ V} = 4,3\text{ V}$$

L'anode de la diode $D_2$ est quant à elle reliée à la source secondaire $V_{\text{cc2}} = 3,0\text{ V}$. La tension aux bornes de $D_2$ ($V_{\text{D2}} = V_{\text{anode2}} - V_{\text{cathode2}}$) est donc :
$$V_{\text{D2}} = 3,0\text{ V} - 4,3\text{ V} = -1,3\text{ V}$$

> **Analyse du blocage :** La tension $V_{\text{D2}}$ étant négative ($-1,3\text{ V}$), la diode $D_2$ est polarisée en inverse. Elle se comporte comme un interrupteur ouvert. La source de $3,0\text{ V}$ est mathématiquement et physiquement isolée du reste du circuit, empêchant tout retour de courant destructeur vers celle-ci.

---

## Mesure des tensions en polarisation directe
<table>
  <tr>
    <td align="center" valign="top">
      <img width="1530" height="2040" alt="Mesure D1" src="https://github.com/user-attachments/assets/45e53645-d447-4381-98ed-2c150aa9cdcf" />
    </td>
    <td align="center" valign="top">
      <img width="1530" height="2040" alt="Mesure LED M3" src="https://github.com/user-attachments/assets/57e23508-e45f-461e-849a-90db9cd20f66" />
    </td>
    <td align="center" valign="top">
      <img width="1530" height="2040" alt="Mesure Resistor M3" src="https://github.com/user-attachments/assets/4f102bc8-281e-40dc-a904-92407ac26aac" />
    </td>
    <td align="center" valign="top">
      <img width="1530" height="2040" alt="Mesure D2" src="https://github.com/user-attachments/assets/44c055bf-2c62-4fae-8421-567f24d8def0" />
    </td>
  </tr>
  <tr>
    <td align="center">tension diode D1</td>
    <td align="center">tension LED</td>
    <td align="center">tension résistor</td>
    <td align="center">tension diode D2</td>
  </tr>
</table>

* **Le circuit :** Connecte deux sources d'alimentation distinctes (une source principale de **5 V** et une source secondaire de **3 V**). Relie la source 5V sur l'anode de la *Diode 1* et la source 3V sur l'anode de la *Diode 2*. Rassemble les deux cathodes ensemble sur une même ligne centrale de la breadboard (nœud commun). Depuis cette ligne de sortie commune, place un résistor de **220\ $\Omega$** suivi d'une LED reliée à la masse commune (GND).
* **L'expérience :** La LED s'allume automatiquement en sélectionnant la tension la plus élevée (le 5V). Si tu débranches la source principale de 5V, la ligne bascule instantanément sur la source secondaire de 3V et la LED reste allumée sans aucune interruption. 
* **Conclusion :** Les diodes agissent comme des clapets anti-retour automatiques commandés par la tension. La source la plus forte bloque la diode de la source la plus faible. Les deux sources d'entrée restent parfaitement isolées l'une de l'autre, empêchant tout retour de courant destructeur de l'une vers l'autre.
