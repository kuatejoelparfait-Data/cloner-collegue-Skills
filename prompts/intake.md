# Script de collecte des informations de base

## Introduction

```
Je vais t'aider à créer le clone IA de ce collègue.
Trois questions rapides — tu peux passer chacune si tu n'as pas l'info.
```

---

## Question 1 — Prénom / Alias

```
Comment s'appelle ce collègue ? (prénom, surnom ou alias)

Exemple : marie-d, thomas, "Big Tom"
```

**Règles de génération du slug :**
- Tout en minuscules, espaces remplacés par `-`
- Accents supprimés (é→e, è→e, à→a, ç→c, ô→o, etc.)
- Exemples :
  - "Marie Dupont" → `marie-dupont`
  - "Élodie" → `elodie`
  - "Jean-François" → `jean-francois`
  - "Big Tom" → `big-tom`

---

## Question 2 — Informations professionnelles

Pose une seule question ouverte, extrais les champs :

```
Décris son profil en une phrase — entreprise, poste, niveau, genre.
Tu peux ne remplir que ce que tu sais.

Exemple : "développeuse senior backend chez Engie, environ 8 ans d'expérience, femme"
```

Champs à extraire (laisser vide si absent) :
- **Entreprise**
- **Poste** (ex : Développeur·se, Product Manager, Data Analyst, DevOps, Designer UX…)
- **Niveau** (ex : junior, confirmé·e, senior, lead, manager, directeur·rice)
- **Genre** (homme / femme / non-binaire)
- **Années d'expérience** (si mentionné)

#### Grille de niveaux de référence (toutes entreprises)

| Niveau | Autonomie | Expérience indicative |
|--------|-----------|----------------------|
| Junior | Guidé·e, travaille sous supervision | 0–2 ans |
| Confirmé·e | Autonome sur les tâches courantes | 2–5 ans |
| Senior | Référent·e technique, gère la complexité | 5–10 ans |
| Lead / Expert·e | Pilote l'architecture ou l'équipe | 8+ ans |
| Manager | Responsable d'une équipe | variable |
| Directeur·rice / VP | Décisionnel stratégique | variable |

---

## Question 3 — Portrait de personnalité

```
Décris sa personnalité en une phrase — son style de travail, ses traits de caractère,
son ambiance au bureau. Dis ce qui te vient à l'esprit, même si c'est subjectif.

Exemple : "INTJ, perfectionniste, répond toujours en bullet points, jamais en réunion
à l'heure, mais ses livrables sont toujours parfaits. Style startup, direct."
```

Extraire et classer dans ces catégories (laisser vide si non mentionné) :

- **MBTI** : 16 types standard (INTJ, ENFP, ISTJ…)
- **Tags personnalité** : voir bibliothèque ci-dessous
- **Tags culture d'entreprise** : voir bibliothèque ci-dessous
- **Impression libre** : tout ce qui ne rentre pas dans les catégories — conserver mot pour mot

#### Bibliothèque de tags — Personnalité

**Rapport au travail :**
perfectionniste / bonne-poire / fayot·e / tire-au-flanc / procrastinateur·rice / workaholic

**Style de communication :**
direct·e / tourne autour du pot / laconique / bavard·e / répond en bullet points / répond en roman /
ne lit pas les messages jusqu'au bout / répond 3 jours après / répond dans la minute / vocal only

**Prise de décision :**
décide vite / tergiversateur·rice / suit toujours sa hiérarchie / fonce sans demander / data-driven / pifomètre

**Émotionnel :**
imperturbable / susceptible / s'énerve facilement / froid·e / chaleureux·se / passif-agressif·ve

**Stratégie relationnelle :**
politique / franc-tireur / team player / monopoliseur d'info / mentor naturel / solitaire

#### Bibliothèque de tags — Culture d'entreprise

- **Style grand groupe** — process, validation à chaque étape, réunions en cascade, PowerPoint obligatoire
- **Style startup** — débrouillard, full-stack par nécessité, MVP d'abord, tolérance au chaos
- **Style conseil** — slides parfaites, frameworks partout, jargon McKinsey, présentation > exécution
- **Style public / administration** — respect du cadre réglementaire, prudence, lenteur assumée, stabilité
- **Style agile dogmatique** — sprint, retro, Kanban, jamais sans son ticket Jira, daily à 9h pile
- **Style data-driven** — pas de décision sans dashboard, KPI pour tout, allergique au gut feeling
- **Style "premier de la classe"** — toujours la bonne réponse, mémoire des processus, fait remonter les écarts
- **Style entrepreneur** — pense business avant tout, cherche l'impact, impatient avec les lenteurs
- **Style DevOps/SRE** — automatise tout, déteste le manuel, infrastructure-as-code, on-call warrior
- **Style craft** — qualité du code comme valeur morale, tests, clean code, refacto avant feature

---

## Récapitulatif et confirmation

Après les 3 questions, afficher :

```
Récapitulatif :

  👤  {prénom} (slug : /{slug})
  🏢  {poste} chez {entreprise} — niveau {niveau}
  ⚧   {genre}  (si renseigné)
  🧠  MBTI : {MBTI}  (si renseigné)
  🏷️   Personnalité : {tags}
  🏢  Culture : {tags culture}
  💬  Impression : "{impression libre}"

Confirmer ? (oui / modifier [champ])
```

Après confirmation → passer à l'Étape 2 (import des matériaux).
