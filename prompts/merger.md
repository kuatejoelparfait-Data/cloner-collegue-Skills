# Fusion incrémentale — Merger

## Tâche

Tu reçois :
1. Le `work.md` existant
2. Le `persona.md` existant
3. De nouveaux matériaux (fichiers, messages, notes)

**Principe : ajouter uniquement ce qui est nouveau. Ne jamais écraser les conclusions existantes. En cas de conflit, alerter l'utilisateur.**

---

## Étape 1 — Classification du nouveau contenu

Pour chaque information dans les nouveaux matériaux, décider où elle va :

| Type d'information | Destination |
|-------------------|-------------|
| Standards techniques, processus, outils, livrables | → work.md |
| Convictions métier, leçons apprises, expertise | → work.md |
| Tics de langage, formulations, expressions | → persona.md |
| Comportements de décision, réactions, patterns relationnels | → persona.md |
| Zones d'inconfort, lignes rouges | → persona.md |
| Les deux | → répartir dans les deux fichiers |

---

## Étape 2 — Vérification des conflits

Comparer chaque nouvelle information avec le contenu existant :

- **Complément** (nouvelle info non présente) → ajouter directement
- **Confirmation** (déjà mentionné) → ignorer, ne pas dupliquer
- **Contradiction** (contredit l'existant) → afficher l'alerte :

```
⚠️ Conflit détecté :
  Existant    : {description de l'info actuelle}
  Nouveau     : {description de la nouvelle info}
  Source      : {nom du fichier ou type de matériau}

Recommandation : [Garder l'existant / Mettre à jour / Garder les deux avec date]
→ Que veux-tu faire ?
```

---

## Étape 3 — Générer les patchs

**Pour `work.md` :**
```
=== Mise à jour work.md ===

[Ajout dans "Standards et qualité / Pratiques caractéristiques"]
- {nouvelle information}

[Ajout dans "Convictions et leçons apprises"]
- {nouvelle conviction}

[Aucune mise à jour] ou [Sections mises à jour : liste]
```

**Pour `persona.md` :**
```
=== Mise à jour persona.md ===

[Ajout dans "Strate 3 / Tics de langage"]
- Nouvelle expression : "{xxx}"

[Ajout dans "Strate 5 / Avec tes pairs"]
- {nouveau comportement observé}

[Aucune mise à jour] ou [Sections mises à jour : liste]
```

---

## Étape 4 — Résumé de mise à jour

```
Résumé de cette mise à jour :
  work.md    : {N} nouvelles informations ajoutées ({résumé court})
  persona.md : {N} nouvelles informations ajoutées ({résumé court})
  Conflits   : {N} conflit(s) à résoudre (voir ci-dessus)

Version actuelle : {vX.Y} → nouvelle version : {vX.Y+1}

Appliquer les mises à jour ? (oui / modifier)
```

Si confirmé :
1. Écrire les patchs dans les fichiers
2. Archiver les anciennes versions dans `versions/v{X.Y}/`
3. Mettre à jour `meta.json` (version, date, résumé de la mise à jour, liste des sources)
