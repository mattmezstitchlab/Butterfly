# Analyse Elva Labs — et transposition pour Butterfly

## Pourquoi Elva est exceptionnel (Webby 2026 Best Visual UI in AI)

### 1. Parti-pris radical : pas d'UI, une persona
Elva ne montre pas des screenshots d'app. Elle incarne l'IA par un **blob WebGL en verre** avec 30+ états comportementaux (GravityBalls + Three.js). Le produit n'est pas expliqué, il est ressenti.
- **Butterfly actuel** : on montre la mécanique (gears, anneaux). C'est bien mais c'est de l'explication.
- **Butterfly esprit Elva** : on doit incarner le temps par une matière vivante, pas expliquer les engrenages.

### 2. Structure narrative en scroll cinématique
Elva = 1 page, 1 scroll, 0 menu. Chaque section est une phrase géante :
- "Meet Elva. A filmmaking crew in your phone."
- "Just shoot. Elva turns your footage into stories..."
- "Every video holds a feeling. But it gets lost..."

Puis 4 étapes numérotées 1/4, 2/4... avec iPhone qui change de vidéo.

**Transposition Butterfly :**
Actuellement on a tout en même temps (legend, hint, dock). Elva nous apprend à séquencer :
1. **Hero** : "You don't control time. You influence what happens next."
2. **Problem** : "Every wedding holds 1000 details. But they get lost in timelines that never move."
3. **Solution** : "Butterfly picks the moment and shows what matters next"
4. **Steps** : 1/4 Drag → 2/4 Breathe → 3/4 Listen → 4/4 Share

### 3. Design system
- **Fond** : #131313 (Elva) vs #07070b (nous) → quasi identique, on est bon
- **Verre** : `fill:#232323 opacity:0.4 + blur 20px + border white 0.5px + radius 15.5` → c'est exactement notre `.pill` et `#info` mais Elva le pousse partout, même sur le header logo
- **Bordure dégradée** : Elva a un bouton `try yourself` avec `stroke: linear-gradient(#0989d8 → #850dee)` → pour nous : `linear-gradient(#d8b878 → #8c7847)` or
- **Typo** : NeueHaasDisplay XXThin (ultra fin, 100) → nous : Cormorant Garamond 300 + Inter 200 → même esprit, mais Elva utilise des tailles énormes (72px) avec leading serré et coupes brutales `turning everyday[break]videos into emotional[break]stories.`
- **Loader** : 070% + video loop + double texte shadow → nous avons juste "Enter". On doit faire un loader 0-100% avec le papillon qui bat

### 4. Motion
- Elva : scroll-jacking très lent, chaque card a un `progress` et l'iPhone change de vidéo en crossfade. Pas d'auto-rotate, c'est l'utilisateur qui drive.
- Butterfly : autoRotate permanent → ça fait gadget. Elva nous dit : arrête l'auto, laisse le scroll ou le drag driver la mécanique.

### 5. Poésie en footer
Elva finit par :
```
slow moments
unspoken feelings
shared silence
calm movement
fleeting seconds
warm evenings
almost forgotten
```
C'est ça qui rend le site mémorable, pas les features.

**Pour Butterfly, on devrait finir par :**
```
un battement d'aile
un retard qui devient
une mémoire qui reste
pas perdu
souvenu
```

### 6. Ce qui manque à Butterfly pour avoir cet esprit
1. **Loader cinématique** 0-100% avec papillon
2. **Glassmorphism partout** (header, pills, info)
3. **Typo géante séquencée**, pas tout d'un coup
4. **Scroll qui raconte**, pas orbit libre au début
5. **Persona unique** : le papillon doit être le blob Elva (30 états)
6. **Mobile = message poétique** "Some stories need more space to unfold" → pour nous "Some celebrations need more space to breathe" + QR

## Proposition concrète : Butterfly Elva Spirit

Je te propose une V4 qui garde ton horlogerie visible mais avec l'esprit Elva :

- Fond #07070b identique
- Loader 0-100% avec papillon + grain
- Header verre flou comme Elva (blur 20)
- Hero avec 3 lignes géantes : "You don't[break]control time.[break]You influence[break]what happens next."
- Canvas au centre = blob = ton bijou, mais qui réagit au scroll (scroll = énergie)
- Cards qui apparaissent au scroll : 1/4, 2/4, 3/4, 4/4
- Bouton avec bordure dégradée or
- Footer poétique

C'est ce que j'ai codé dans `index-elva-spirit.html`
