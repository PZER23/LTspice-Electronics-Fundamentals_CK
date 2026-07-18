# A) C'est quoi un condensateur ?

<table>
  <tr>
    <td align="center" valign="top">
    <img width="450" height="135" alt="cap_all2" src="https://github.com/user-attachments/assets/b3dbecfb-10f2-4ade-a2b9-b5bf2f3d4b82" />
</td>
    <td align="center" valign="top">
<img width="135" height="135" alt="images" src="https://github.com/user-attachments/assets/4d7fdd17-9312-4980-b697-0eda80a2a692" />
    </td>
  </tr>
</table>

## 1. Définition
Un condensateur est un composant électronique passif (un dipôle) capable de stocker temporairement de l'énergie électrique sous la forme d'un champ électrique, afin de la restituer plus tard. Physiquement, il est constitué de deux armatures conductrices (généralement des plaques métalliques) placées face à face et séparées par un matériau isolant appelé le **diélectrique** (qui peut être de l'air, de la céramique, du plastique, du mica, etc.).

## 2. Rôle dans un circuit
Le rôle principal du condensateur est d'agir comme un réservoir d'énergie à réaction ultra-rapide ou une micro-batterie temporaire. Pour bien le conceptualiser, on utilise l'analogie d'un réservoir d'eau muni d'une membrane élastique au milieu d'une canalisation :

*   **Il accumule** les charges électriques quand il y a un flux de courant (le réservoir se remplit).
*   **Il restitue** instantanément cette électricité dès que la tension du circuit baisse (le réservoir se vide pour compenser le manque).

Contrairement à une batterie chimique classique, il peut se charger et se décharger en une fraction de seconde (quelques millisecondes) et supporte des millions de cycles de charge sans s'user.

## 3. Principe de fonctionnement
Lorsqu'on applique une tension continue aux bornes du condensateur :

*   **En phase de charge (Polarisation) :** Les électrons (charges négatives) poussés par la source d'alimentation viennent s'accumuler en masse sur l'une des plaques. Par effet d'influence, l'autre plaque se vide de ses électrons et devient chargée positivement. Les charges opposées s'attirent fortement à travers l'isolant central, mais le diélectrique les empêche de traverser. Un champ électrique se forme alors entre les plaques, emprisonnant l'énergie. Le condensateur arrête sa charge dès que sa tension interne égale celle de l'alimentation.
*   **En phase de décharge :** Si on débranche l'alimentation et qu'on ferme le circuit sur un autre composant (comme une LED ou un résistor), les électrons accumulés sur la plaque négative se précipitent dans le circuit pour rejoindre la plaque positive et rétablir l'équilibre. Le condensateur libère alors toute son énergie stockée jusqu'à être complètement vide.

## 4. Caractéristiques fondamentales

* **a) La capacité ($C$) :** C'est la grandeur physique qui mesure l'aptitude du condensateur à stocker des charges électriques. Plus la capacité est grande, plus le réservoir est volumineux. Elle se mesure en **Farads ($F$)**. Le Farad étant une unité gigantesque, on utilise principalement ses sous-multiples :
  * Le microfarad ($\mu\text{F} = 10^{-6}\text{ F}$)
  * Le nanofarad ($\text{nF} = 10^{-9}\text{ F}$)
  * Le picofarad ($\text{pF} = 10^{-12}\text{ F}$)
  * La formule fondamentale associée est :
    $Q = C \times U$ (où $Q$ est la charge en Coulombs, $C$ la capacité en Farads, et $U$ la tension en Volts)

* **b) La capacité équivalente ($C_{eq}$) :** Lorsqu'on associe plusieurs condensateurs, le calcul de la capacité totale (équivalente) suit les règles **strictement inverses** de celles des résistors :
  * **En Parallèle :** Les capacités s'additionnent (on augmente la surface des armatures conductrices, donc le volume du réservoir).
    $$C_{eq} = C_1 + C_2 + C_3 + \dots$$
  * **En Série :** On applique la loi des inverses (on augmente l'épaisseur globale de l'isolant diélectrique, ce qui diminue la capacité globale). La capacité équivalente est toujours plus petite que le plus petit condensateur du groupe.
    $$\frac{1}{C_{eq}} = \frac{1}{C_1} + \frac{1}{C_2} + \frac{1}{C_3} + \dots$$

* **c) La tension maximale d'utilisation ($V_{max}$ ou Rated Voltage) :** C'est la tension limite absolue que le diélectrique peut encaisser. Si la tension à ses bornes dépasse cette valeur, l'isolant subit un "claquage". Un arc électrique traverse alors le composant, créant un court-circuit interne destructeur (le condensateur peut éclater ou exploser).
  * *Astuce de circuit :* Associer deux condensateurs identiques en série permet de doubler la tension maximale qu'ils peuvent supporter ensemble (la tension se divise équitablement entre eux).

* **d) La polarité :** Certains condensateurs doivent obligatoirement être branchés dans un sens précis (la patte la plus longue sur le pôle positif $+$, et la bande portant des symboles $-$ sur le pôle négatif). Une inversion de polarité sur ces modèles peut provoquer leur destruction rapide. D'autres modèles (céramiques, films) sont non polarisés et s'insèrent dans n'importe quel sens.

* **e) La Résistance Série Équivalente (ESR) :** C'est la résistance interne parasite du condensateur. Une ESR très faible est cruciale dans les circuits où le condensateur doit réagir extrêmement vite (haute fréquence) ou manipuler de forts courants sans surchauffer.

* **f) La tolérance :** Tout comme pour les résistors, c’est l’écart maximal acceptable en pourcentage (ex: $\pm10\%$ ou $\pm20\%$) entre la capacité réelle du composant sorti d'usine et la valeur théorique imprimée sur son boîtier.

---

# B) Les variantes du composant
Voici les types de condensateurs incontournables, tous au format "traversant" (*Through-Hole*), que tu peux facilement manipuler sur ta plaque d'essai :

### 1. Le condensateur électrolytique (Aluminium) : *Le réservoir géant*
C'est le modèle le plus visible : un petit cylindre vertical (souvent noir ou bleu) marqué d'une bande grise indiquant le côté négatif. Il offre de très grandes capacités (de $1\ \mu\text{F}$ à plusieurs milliers de $\mu\text{F}$) mais il est polarisé. Il est idéal pour filtrer les basses fréquences et stabiliser les alimentations générales.

### 2. Le condensateur céramique : *Le sprinter rapide*
Souvent en forme de petite pastille ou de disque marron/orange monté sur deux pattes fines. Il possède de faibles capacités (du $\text{pF}$ à quelques centaines de $\text{nF}$) mais il est non polarisé et extrêmement réactif. On le place au plus près des circuits intégrés pour éliminer les parasites électriques à haute fréquence (condensateur de découplage).

### 3. Le condensateur à film plastique (Polyester / Mylar) : *Le stable*
De forme souvent rectangulaire ou cubique (jaune, rouge ou bleu), il est non polarisé. Il offre une excellente stabilité face aux variations de température et au vieillissement. Très prisé dans les applications audio (filtres de signal) ou les circuits oscillants de précision.

### 4. Le supercondensateur : *L'ultra-réservoir*
Un composant à la frontière entre le condensateur et la batterie. Il affiche des capacités phénoménales (de $1\ \text{F}$ à plus de $100\ \text{F}$ !), mais sous une tension de service très basse (généralement $2,7\ \text{V}$ ou $5,5\ \text{V}$). On s'en sert comme batterie de secours pour alimenter temporairement une horloge interne ou sauvegarder des données lors d'une coupure.

---

# C) Montages illustrant le rôle du condensateur
Voici trois expériences simples et très visuelles à réaliser pour mettre en valeur les fonctions reines du condensateur sur une breadboard :

## Montage 1 : La Temporisation RC (L'effet micro-batterie)

<table>
  <tr>
    <td align="center" valign="middle">
    <img width="300" height="300" alt="WhatsApp Image 2026-07-18 at 17 20 03" src="https://github.com/user-attachments/assets/3a0a67bd-6469-4421-bb20-72e5a18258c2" />
      <video src="https://github.com/user-attachments/assets/3d7367b4-87fc-4b87-a97e-b6dc049f9aed" width="300" height="300" controls></video>    
    </td>
    <td valign="middle" style="padding-left: 20px;">
      <h3>Composants du circuit :</h3>
      <ul>
        <li>1 Résistor de 220 $\Omega$</li>
        <li>1 condensateur electrolytique de  $100\ \mu\text{F}$ </li>
        <li>1 DEL rouge</li>
        <li>1 resistor de 10 k $\Omega$</li>
        <li>1 Alimentation de 5 V</li>
      </ul>
    </td>
  </tr>
</table>
Ce montage met en lumière la vitesse de charge et de décharge contrôlée du composant à travers une résistance.

*   **Le circuit :** Alimentation $5\text{V} \rightarrow$ Bouton-poussoir $\rightarrow$ Résistance de $10\ \text{k}\Omega \rightarrow$ Condensateur électrolytique de $100\ \mu\text{F}$ (borne `+` connectée à la résistance, borne `-` reliée au GND). Connecte également en parallèle aux bornes de ce condensateur une résistance de $220\ \Omega$ en série avec une LED classique branchée vers le GND.
*   **L'expérience :** 
    1. Maintiens le bouton enfoncé : la LED s'allume immédiatement tandis que le condensateur accumule l'énergie.
    2. Relâche le bouton : au lieu de s'éteindre instantanément, la LED reste allumée puis faiblit très progressivement pendant quelques secondes avant de s'éteindre totalement.
*   **Mesure au multimetre :**
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
> **Conclusion (pour GitHub) :** Lorsque le bouton est relâché, le condensateur prend le relais de l'alimentation et fournit son énergie stockée à la LED en se vidant lentement à travers la résistance de $10\ \text{k}\Omega$. C'est le principe fondamental des minuteries ou des circuits de délai.

## Montage 2 : Le Filtrage d'Alimentation (L'amortisseur de tension)
Ce montage illustre comment un condensateur immunise un circuit contre les micro-coupures électriques ou les chutes de tension brusques.

*   **Le circuit :** Réalise un circuit simple : Alimentation $5\text{V} \rightarrow$ Résistance de $220\ \Omega \rightarrow$ LED $\rightarrow$ GND. La LED s'allume de manière fixe.
*   **L'expérience :**
    1. Fais glisser rapidement le fil d'alimentation du $5\text{V}$ pour simuler un faux contact ou une coupure très brève : la LED s'éteint net ou clignote.
    2. Ajoute maintenant un gros condensateur électrolytique de $1000\ \mu\text{F}$ directement sur les rails d'alimentation généraux de ta breadboard (`+` sur la ligne rouge VCC, `-` sur la ligne bleue GND). Refais la même micro-coupure : la LED ne cille même pas, son éclat reste parfaitement constant !

> **Conclusion (pour GitHub) :** Le condensateur agit comme un régulateur de choc électrique. Lors de la coupure, il libère instantanément son énergie interne pour combler le manque de courant, maintenant une tension parfaitement lisse et propre pour le reste du circuit.

## Montage 3 : Le blocage du Courant Continu (Couplage et transmission de signal)
Ce montage prouve qu'un condensateur bloque le courant continu constant (DC) mais s'ouvre pour laisser passer les variations de signaux (AC/Impulsions).

*   **Le circuit :** Relie un bouton-poussoir au $5\text{V}$. Sa sortie se connecte sur une patte d'un condensateur céramique ou à film de $100\ \text{nF}$. L'autre patte du condensateur est branchée à une résistance de $10\ \text{k}\Omega$ qui va au GND. Connecte les pointes de ton multimètre (en mode Voltmètre DC) aux bornes de la résistance de $10\ \text{k}\Omega$.
*   **L'expérience :**
    1. Appuie sur le bouton et maintienne ton doigt enfoncé. Tu verras la tension sur le voltmètre sauter brièvement à l'instant du clic, puis retomber à $0\ \text{V}$ instantanément, même si le bouton reste pressé. Le courant continu stable est totalement bloqué une fois le condensateur chargé.
    2. Appuie et relâche le bouton très rapidement et de manière répétée : à chaque clic et à chaque relâchement (les phases de transition), le multimètre détecte une impulsion électrique nette.

> **Conclusion (pour GitHub) :** Le condensateur se comporte comme une barrière hermétique pour le courant continu établi, mais devient transparent dès qu'un signal varie (changement d'état). C'est indispensable pour isoler des signaux audio de leur alimentation continue ou pour concevoir des détecteurs d'impulsions logiques.
