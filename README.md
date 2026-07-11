# 🎹 Piano · Méthode en douze semaines

Un cours de piano interactif pour débutant, conçu autour d'un **clavier Arturia
KeyLab Essential 49** et de trente minutes de pratique par jour. Objectif : en
trois mois, jouer à deux mains, composer ses propres accords, et comprendre la
théorie derrière ce qu'on fait — sans se noyer.

**[▶ Ouvrir la méthode](https://vecrea.github.io/piano-arthur/)** *(actif dès
que GitHub Pages est activé — voir plus bas)*

---

## Ce que contient la méthode

**Un programme en 12 semaines, 4 modules :**

| Module | Semaines | Objectif |
| --- | --- | --- |
| **I · Fondations** | 1 → 3 | Repérer les notes, tenir un tempo, coordonner les deux mains |
| **II · Théorie & premiers accords** | 4 → 6 | Gammes majeures, triades, renversements et progressions pop |
| **III · Deux mains, vraiment** | 7 → 9 | Patterns d'accompagnement, mélodie + accords, premier morceau complet |
| **IV · Jazz & composition** | 10 → 12 | Accords de 7e, blues en 12 mesures, composer 16 mesures à soi |

Chaque semaine : un objectif clair, 3 à 4 exercices minutés, une aparté "à
écouter", et une case à cocher qui sauvegarde ton avancement.

**Un instrument virtuel :**

- Clavier SVG de 49 touches (C2 → C6, le range exact du KeyLab Essential 49)
- Détection MIDI en direct via [Web MIDI API](https://developer.mozilla.org/en-US/docs/Web/API/Web_MIDI_API) — branche l'USB et joue
- Synthèse audio en temps réel via [Web Audio API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API) (le KeyLab est un contrôleur sans son intégré)
- Pédale sustain (MIDI CC64) prise en charge
- Sans câble : clavier QWERTY (Q = Do central) ou clic sur les touches

**Des outils de référence :**

- Bibliothèque de 90+ accords cliquables : majeurs, mineurs, 7, maj7, m7, sus2, sus4, diminués, 9e
- Visualiseur de gammes (majeure, mineure naturelle et harmonique, dorien,
  mixolydien, pentatoniques, blues, chromatique) sur les 12 tonalités
- Cercle des quintes cliquable
- Tableau des intervalles
- Cadences essentielles (V-I, IV-I, ii-V-I) prêtes à écouter

**Sauvegarde locale :** l'avancement des exercices et la préférence de thème
sont stockés dans `localStorage`. **Rien n'est envoyé nulle part.**

## Utilisation

### En local

```bash
git clone https://github.com/vecrea/piano-arthur.git
cd piano-arthur
# Ouvre index.html dans un navigateur — voilà.
```

Aucun serveur, aucun build, aucune dépendance. Un simple double-clic sur
`index.html` fonctionne, mais pour la détection MIDI il vaut mieux servir le
fichier via `http://` — un simple `python3 -m http.server` suffit :

```bash
python3 -m http.server 8000
# puis ouvre http://localhost:8000
```

### Détection MIDI

- Navigateur compatible : **Chrome**, **Edge**, ou **Opera** (Web MIDI n'est
  pas encore supporté sur Safari et Firefox stable)
- Branche le KeyLab Essential 49 en USB avant d'ouvrir la page
- Autorise l'accès MIDI dans la boîte de dialogue du navigateur
- Le badge en haut à droite passe au vert quand ton piano est détecté

### Déployer en ligne (GitHub Pages)

1. **Settings → Pages**
2. **Source : Deploy from a branch**
3. **Branch : `main`**, dossier : `/ (root)`
4. Sauvegarde. La page est en ligne à
   `https://vecrea.github.io/piano-arthur/` en une minute.

## Architecture

Un unique fichier `index.html` :

- ~120 Ko, ~3000 lignes
- Zéro dépendance externe (les polices utilisent des stacks système)
- HTML + CSS + JavaScript inline
- Aucun code de tracking, aucune requête réseau
- Fonctionne offline une fois le fichier chargé

Ce choix est délibéré. Le single-file :

- Marche même hors ligne
- Se sauvegarde et se partage comme un PDF
- N'impose aucun build ni environnement
- Se déploie sur n'importe quel hébergeur qui sert du HTML

## Design

Palette inspirée des programmes de concert et des couvertures de méthodes
anciennes — ivoire de papier vieilli, encre profonde, laiton bruni, bourgogne.
Typographie : Playfair Display et Georgia, sans dépendance à un font CDN.
Thème clair et sombre. Responsive du téléphone au grand écran.

## Roadmap

Améliorations possibles pour plus tard :

- [ ] Métronome intégré (avec réglage BPM)
- [ ] Support du mode chromatique complet sur les gammes exotiques
- [ ] Sauvegarde du dernier morceau composé (module 12)
- [ ] Version anglaise
- [ ] Enregistrement audio de sa performance

## Licence

MIT — voir [`LICENSE`](LICENSE).

---

*Édition privée · MMXXVI · Fait à la main pour Arthur.*
