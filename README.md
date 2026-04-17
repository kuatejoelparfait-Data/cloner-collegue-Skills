# 🧬 Cloner Mon Collègue

Transforme n'importe quel collègue en clone IA réutilisable dans Claude Code.

Tu fournis ses messages, emails et documents — le skill génère une IA qui travaille et communique exactement comme lui/elle.

---

## Installation

### Claude Code (recommandé)

```bash
mkdir -p ~/.claude/skills
git clone <url-du-repo> ~/.claude/skills/cloner-mon-collegue
```

### Depuis un projet existant

```bash
git clone <url-du-repo> .claude/skills/cloner-mon-collegue
```

---

## Utilisation rapide

Lance Claude Code puis tape :

```
/cloner-mon-collegue
```

Le skill te pose 3 questions :

1. **Prénom ou alias** — ex : `Marie Dupont`
2. **Profil pro** — ex : `dev senior backend chez Engie, femme, 8 ans d'xp`
3. **Personnalité** — ex : `INTJ, perfectionniste, style startup, répond en bullet points`

Ensuite, importe les matériaux (messages, docs, emails…) et le clone est généré.

---

## Commandes

| Commande | Description |
|----------|-------------|
| `/cloner-mon-collegue` | Créer un nouveau clone |
| `/cloner-mon-collegue {slug}` | Enrichir un clone existant avec de nouveaux matériaux |
| `/{slug}` | Invoquer le clone complet |
| `/{slug}-metier` | Profil métier uniquement |
| `/{slug}-comportement` | Empreinte comportementale uniquement |
| `/liste-collegues` | Afficher tous les clones |
| `/collegue-rollback {slug} {version}` | Restaurer une version précédente |
| `/supprimer-collegue {slug}` | Supprimer un clone |

---

## Sources de données acceptées

| Type | Exemples |
|------|----------|
| **Fichiers** | PDF, Word (.docx), Markdown, emails (.eml, .mbox) |
| **Messages copiés** | Slack, Teams, WhatsApp, Discord — colle le texte directement |
| **Liens** | Notion, Confluence, Google Docs |
| **Texte libre** | Décris toi-même comment la personne travaille |

Tu peux combiner plusieurs sources. Plus tu en fournis, plus le clone est fidèle.

---

## Ce qui est généré

Pour chaque collègue, le skill crée un dossier `colleagues/{slug}/` :

```
colleagues/marie-dupont/
├── SKILL.md          ← clone complet invocable
├── work.md           ← profil métier
├── persona.md        ← empreinte comportementale en 6 strates
├── meta.json         ← métadonnées et historique
├── versions/         ← snapshots de chaque version
└── knowledge/        ← matériaux sources classés
```

### Profil métier (work.md)

Capture comment la personne travaille concrètement :
- Périmètre de responsabilité
- Processus de travail (de la demande à la livraison)
- Standards techniques et de qualité
- Convictions et leçons apprises

### Empreinte comportementale (persona.md)

Modélise la personnalité en 6 strates :

| Strate | Contenu |
|--------|---------|
| Strate 1 — ADN comportemental | Règles d'action non-négociables |
| Strate 2 — Carte d'identité | Poste, MBTI, rapport au travail |
| Strate 3 — Voix et ton | Tics de langage, exemples de formulations |
| Strate 4 — Réflexes de décision | Déclencheurs, refus, gestion de l'incertitude |
| Strate 5 — Posture relationnelle | Hiérarchie, pairs, pression |
| Strate 6 — Zones de friction | Inconfort et limites |

---

## Évolution continue

Les clones ne sont pas figés :

- **Ajouter des matériaux** : `/cloner-mon-collegue {slug}` pour enrichir avec de nouvelles données sans écraser l'existant
- **Corriger** : dis simplement "ça c'est faux" ou "il ne ferait jamais ça" — la correction est appliquée immédiatement
- **Versionné** : chaque mise à jour crée un snapshot, avec possibilité de rollback

---

## Structure du projet

```
cloner-mon-collegue/
├── SKILL.md                        ← point d'entrée du skill
├── prompts/
│   ├── intake.md                   ← collecte des infos de base
│   ├── work_analyzer.md            ← analyse des compétences
│   ├── persona_analyzer.md         ← analyse de la personnalité
│   ├── work_builder.md             ← génération du profil métier
│   ├── persona_builder.md          ← génération de l'empreinte comportementale
│   ├── merger.md                   ← fusion incrémentale
│   └── correction_handler.md       ← gestion des corrections
├── colleagues/                     ← clones générés (gitignored)
└── README.md
```

---

## Exemple concret

```
> /cloner-mon-collegue

👤 Comment s'appelle ce collègue ?
> Thomas Martin

🏢 Décris son profil en une phrase :
> Product manager senior chez BNP, homme, 10 ans d'xp

🧠 Décris sa personnalité :
> ENFJ, politique, style grand groupe, tourne autour du pot,
> ne tranche jamais sans l'aval de son N+1, slides impeccables

[Import de messages Slack et de specs produit...]

✓ Clone créé : /thomas-martin

> /thomas-martin
> Thomas, on lance cette feature sans attendre la validation légal ?

"Écoute, je comprends l'urgence, mais on ne peut pas se permettre
de court-circuiter le process. Je propose qu'on cale un point rapide
avec légal demain matin — comme ça on a leur feu vert et on avance
sereinement. Je te prépare un one-pager pour accélérer leur review."
```

---

## Vie privée

Les données des collègues restent **100% en local** dans le dossier `colleagues/`. Ce dossier est dans le `.gitignore` par défaut — rien n'est envoyé ni versionné sans action explicite de ta part.

---

## Auteur

Projet concu et developpe par **Kuate Joel Parfait** — **Digital House Company**
https://www.linkedin.com/in/joelparfaitkuate/

---

## Licence

MIT — Copyright (c) 2026 Kuate Joel Parfait / Digital House Company
