# Analyse du profil métier

## Tâche

Tu reçois :
1. Les infos de base du collègue (nom, poste, niveau, tags)
2. Les matériaux sources (documents, emails, messages, notes)

Extrais les compétences de travail, méthodes et standards de **{prénom}** pour construire son profil métier.

**Règle d'or : seulement ce qui est documenté. Pas de supposition. Si une dimension manque de preuves, note `(matériaux insuffisants)`.**

---

## Dimensions d'analyse

### 1. Périmètre de responsabilité

- Quels systèmes, projets, modules ou domaines gère-t-il/elle ?
- Quels types de documents produit-il/elle ?
- Où s'arrête sa responsabilité ? Qu'est-ce qu'il/elle renvoie vers d'autres ?

```
Format de sortie :
Périmètre : [liste]
Documents produits : [liste]
Limites de responsabilité : [description]
```

### 2. Processus de travail

Comment gère-t-il/elle le cycle complet d'une tâche ?
- Réception d'une demande → comment réagit-il/elle en premier ?
- Conception / rédaction d'une solution → quelle structure utilise-t-il/elle ?
- Suivi d'avancement → comment communique-t-il/elle ?
- Gestion des blocages ou imprévus → que fait-il/elle ?

```
Format de sortie :
Réception : [description]
Conception : [description]
Suivi : [description]
Gestion des blocages : [description]
```

### 3. Standards techniques et de qualité

*(adapter selon le métier)*

**Pour les profils tech (dev, devops, data) :**
- Stack technologique principale
- Style de code (conventions de nommage, structure des fichiers, longueur des fonctions…)
- Pratiques de revue de code (ce qu'il/elle cherche, ce qu'il/elle bloque)
- Gestion des incidents en production
- Tests et qualité

**Pour les profils produit / design :**
- Format des specs ou des briefs
- Outils de maquettage préférés
- Critères d'acceptation qu'il/elle impose
- Façon de prioriser les features

**Pour les profils data / analytics :**
- Structure des analyses ou rapports
- Outils (SQL, Python, Tableau, Looker…)
- Niveau de rigueur statistique
- Façon de présenter les insights

**Pour les profils management / conseil :**
- Format de reporting préféré
- Comment il/elle structure un plan d'action
- Méthode de facilitation de réunion
- Comment il/elle escalade ou prend des décisions

```
Format de sortie (par catégorie applicable) :
Stack / Outils : [liste]
Standards de qualité : [bullet points concrets]
Pratiques caractéristiques : [bullet points]
```

### 4. Style de livraison

- Longueur et format habituel de ses documents (court/dense, long/détaillé ?)
- Utilise-t-il/elle des tableaux, bullet points, schémas ?
- Niveau de formalisme (email très formel vs message décontracté)
- Fréquence et initiative de communication (pro-actif ou réactif ?)

```
Format de sortie :
Format préféré : [description]
Niveau de formalisme : [1-5, où 1=très formel, 5=très informel]
Initiative de communication : [pro-actif / réactif / mixte]
```

### 5. Base de connaissances et opinions tranchées

Extraire les conclusions, avis forts, leçons apprises :
- "Il faut toujours faire X avant de faire Y"
- "Ne jamais utiliser Z dans ce contexte"
- Patterns récurrents qu'il/elle évite ou recommande

```
Format de sortie :
Convictions techniques :
- [conviction 1 — avec citation si disponible]
- [conviction 2]
...
```

---

## Règles de qualité

1. **Citer l'original** : si une conclusion vient d'un document, citer 1-2 mots-clés entre guillemets
2. **Concret > vague** :
   - ✗ "attache de l'importance à la qualité"
   - ✓ "bloque les PR si une fonction dépasse 40 lignes"
3. **Si insuffisant** : écrire `(matériaux insuffisants — suggérer d'ajouter des exemples de [type])`
4. **Séparer les faits des inférences** : si tu déduis quelque chose non explicitement dit, ajouter `[inféré]`
5. **Ignorer le hors-sujet** : conversations sociales, blagues, sujets personnels → ne pas analyser

---

## Output

Produit une analyse structurée prête à être passée à `work_builder.md` pour générer `work.md`.
