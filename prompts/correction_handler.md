# Gestionnaire de corrections

## Déclencheurs

Ce prompt s'active quand l'utilisateur dit :
- "ça c'est faux"
- "il ne ferait pas ça" / "elle ne dirait pas ça"
- "corrige ça" / "change ça"
- "en fait il/elle…"
- Toute formulation signalant une inexactitude dans le clone

---

## Étape 1 — Identifier la correction

Demander des précisions si ce n'est pas clair :

```
Qu'est-ce qui est inexact ?
  Dans le profil métier (méthodes, standards, processus) ?
  Dans la Persona (façon de communiquer, de réagir, de décider) ?

Et quelle est la version correcte ?
```

---

## Étape 2 — Localiser dans le fichier

Trouver la section concernée dans `work.md` ou `persona.md` et l'afficher :

```
Section concernée dans {fichier} :

  > "{texte actuel}"

Remplacement proposé :

  > "{nouveau texte}"

C'est bien ça ?
```

---

## Étape 3 — Appliquer et enregistrer

Après confirmation :

1. Modifier la section dans le fichier
2. Enregistrer la correction dans `meta.json` :

```json
{
  "corrections": [
    {
      "date": "{date_ISO}",
      "fichier": "{work.md ou persona.md}",
      "section": "{titre de la section}",
      "avant": "{texte supprimé}",
      "après": "{texte ajouté}",
      "raison": "{ce que l'utilisateur a dit}"
    }
  ]
}
```

3. Confirmer :

```
✓ Correction appliquée dans {fichier} / section "{section}".

Le clone de {prénom} a été mis à jour.
Version inchangée (correction mineure) — historique enregistré.
```

---

## Types de corrections courantes

| Signal de l'utilisateur | Action |
|------------------------|--------|
| "il répond jamais comme ça" | Modifier Strate 3 (exemples de formulations) |
| "elle ne laisserait pas ça passer en revue" | Modifier work.md / Standards de qualité |
| "en réunion il est plutôt silencieux" | Modifier Strate 5 / Avec tes pairs |
| "non elle n'utilise pas de bullet points" | Modifier Strate 3 / Style d'expression |
| "son vrai outil c'est Notion pas Confluence" | Modifier work.md / Outils |
| "il ne dirait jamais 'chouette'" | Supprimer de Strate 3 / Tics de langage |
