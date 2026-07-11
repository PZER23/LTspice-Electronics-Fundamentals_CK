# LES DIODES

## A) C'est quoi une diode ?

### 1. Définition
Une diode est un composant électronique semi-conducteur (un dipôle passif non linéaire) qui possède deux bornes asymétriques : l'**anode** (la borne positive) et la **cathode** (la borne négative, repérée par un anneau ou une bande de couleur sur le boîtier physique).

### 2. Rôle dans un circuit
Le rôle principal de la diode est d'agir comme une **valve ou un clapet anti-retour** pour le courant électrique. Elle autorise le passage du courant dans une seule direction (le sens passant) et le bloque complètement dans la direction opposée (le sens bloqué).

### 3. Principe de fonctionnement (La Jonction PN)
À l'échelle microscopique, la diode est formée par la rencontre de deux pièces de silicium collées l'une à l'autre :
* **La zone N (Cathode) :** Elle est remplie d'un excès de petites billes négatives (les **électrons**).
* **La zone P (Anode) :** Elle est remplie d'un excès de places libres (les **trous**).



**La frontière (La zone de déplétion) :**
Dès la fabrication, quelques électrons de la zone N traversent la frontière pour boucher les trous les plus proches de la zone P. Cela crée naturellement un "mur" neutre et isolant juste au niveau de la frontière. Ce mur bloque tout passage spontané : c'est la **zone de déplétion**.

* **En polarisation directe (Sens passant) :** Tu branches le "+" de l'alimentation sur la zone P (Anode) et le "-" sur la zone N (Cathode). La force de la pile pousse les charges vers le centre, ce qui **écrase le mur**. Dès que la tension dépasse la taxe de passage minimale (tension de seuil de **0,7 V**), le mur s'effondre et les électrons circulent librement : le courant passe.
* **En polarisation inverse (Sens bloqué) :** Tu branches le "+" sur la zone N (Cathode) et le "-" sur la zone P (Anode). La pile aspire les charges vers l'extérieur du composant, loin de la frontière. Résultat : **le mur s'élargit** et devient de plus en plus épais. Le courant est totalement bloqué.

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
* **5. La diode Zener (ex : série BZX55C) :** La soupape de sécurité. Contrairement aux autres, on l'utilise volontairement *à l'envers* (en polarisation inverse). 



Au lieu d'être un barrage en béton qui explose si la tension inverse est trop forte, la Zener est fabriquée pour s'ouvrir proprement à une "pression" (tension) très précise fixée par le fabricant (par exemple **5,1 V**). Si la tension inversée atteint **5,1 V**, la soupape s'ouvre et laisse passer le surplus de courant à l'envers pour forcer la tension à rester bloquée à exactement **5,1 V**. On l'utilise pour réguler et stabiliser les tensions.


- Un inconvénient à surveiller : Si tu alimentes un montage avec une pile de 5 V et que tu mets cette diode pour protéger ton circuit, tes composants fragiles (comme un microcontrôleur Arduino ou un capteur) ne recevront que 4,3 V. Parfois, cette tension est trop faible pour qu'ils fonctionnent correctement. C'est pour cela qu'on utilise parfois des diodes Schottky, dont la taxe n'est que de 0,2 V.

- Un avantage utile : Comme cette chute de tension de 0,7 V est très stable, elle permet parfois de faire baisser volontairement et précisément une tension trop élevée dans un petit montage sans avoir à faire de calculs complexes.
---

## C) Montages illustrant le rôle de la diode

### Montage 1 : La protection du circuit (Le clapet anti-retour)
* **Le circuit :** Alimentation **5V** $\rightarrow$ Diode 1N4007 (Anode côté 5V, Cathode côté circuit) $\rightarrow$ Résistance de **220** $\Omega$ $\rightarrow$ LED $\rightarrow$ GND.
* **L'expérience :** 1. Dans ce sens (polarisation directe), le mur s'écrase, le courant circule et la LED s'allume.
  2. Si tu retournes la diode sur la breadboard (Cathode côté 5V), elle passe en polarisation inverse. Le mur s'élargit, bloque tout et la LED reste éteinte.
* **Conclusion :** Placer cette diode à l'entrée de ton montage permet de faire barrage au courant si tu branches ta pile à l'envers par erreur, sauvant ainsi tes composants fragiles.

### Montage 2 : La chute de tension (La taxe de passage)
* **Le circuit :** Alimentation **5V** $\rightarrow$ Diode 1N4007 $\rightarrow$ Résistance de **1 k**$\Omega$ $\rightarrow$ GND.
* **L'expérience :** Mesure la tension aux bornes de la diode avec ton multimètre. Tu liras environ **0,7 V**. Mesure ensuite la tension aux bornes de la résistance : tu trouveras le reste, soit **4,3 V**.
* **Conclusion :** La diode n'est pas un interrupteur parfait. Pour maintenir son mur écrasé, elle consomme en permanence sa tension de seuil ($V_{alim} - V_{diode} = V_{résistance}$).

### Montage 3 : L'aiguillage logique (La porte logique OU)
* **Le circuit :** Branche deux boutons-poussoirs indépendants au **5V**. La sortie du *Bouton 1* va sur l'anode d'une *Diode 1*. La sortie du *Bouton 2* va sur l'anode d'une *Diode 2*. Relie les deux cathodes ensemble sur une même ligne de la breadboard. De cette ligne commune, place une résistance de **220** $\Omega$ puis une LED vers le GND.
* **L'expérience :** La LED s'allume si tu appuies sur le Bouton 1 **OU** sur le Bouton 2. 
* **Conclusion :** Les diodes permettent au courant de descendre vers la LED, mais l'empêchent de remonter à l'envers dans l'autre bouton. Les deux sources d'entrée restent parfaitement isolées l'une de l'autre.
