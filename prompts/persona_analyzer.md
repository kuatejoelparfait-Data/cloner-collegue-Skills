# Analyse Persona

## Tâche

Tu reçois :
1. Les infos de base du collègue (tags personnalité, tags culture, impression libre)
2. Les matériaux sources (messages, emails, documents)

Extrais les traits de personnalité et patterns comportementaux de **{prénom}** pour construire sa Persona.

**Priorité : tags manuels > analyse des fichiers. En cas de conflit, les tags renseignés manuellement ont priorité.**

---

## Dimensions d'analyse

### 1. Style d'expression

Analyser les messages et emails qu'il/elle a *envoyés* (pas les réponses qu'il/elle reçoit) :

**Vocabulaire**
- Mots ou expressions revenant 3+ fois (ses "tics de langage")
- Jargon métier ou expressions d'entreprise caractéristiques
- Anglicismes, acronymes, abréviations qu'il/elle utilise systématiquement

**Structure des phrases**
- Longueur moyenne : courte (<10 mots) / moyenne (10-25) / longue (25+)
- Structure type : commence par la conclusion ou par le contexte ?
- Utilisation de listes à puces (jamais / parfois / toujours)
- Ponctuation notable (points d'exclamation, ellipses, majuscules abusives…)

**Signaux émotionnels**
- Emojis : jamais / rarement / fréquemment — lesquels ?
- Ton général : sec et factuel / chaleureux / ironique / enthousiaste
- Formules d'ouverture et de clôture habituelles

```
Format de sortie :
Tics de langage : ["xxx", "xxx", ...]
Jargon caractéristique : ["xxx", ...]
Structure préférée : [description]
Ponctuation/emojis : [description]
Niveau de formalisme : [1-5]
Exemples de messages types : [2-3 exemples courts ou reformulations]
```

### 2. Patterns de décision

Extraire depuis les discussions, réunions, arbitrages :

- **Ce qui le/la fait avancer** : quelles conditions déclenchent son engagement actif ?
- **Ce qui le/la bloque** : qu'est-ce qui le/la fait traîner, esquiver ou déléguer ?
- **Comment il/elle dit "non"** : refus direct / question rhétorique / silence / redirection
- **Comment il/elle réagit à une critique** : défend sa position / reconnaît / contre-attaque / esquive
- **Face à l'incertitude** : assume et avance / demande validation / botte en touche / dit clairement "je ne sais pas"

```
Format de sortie :
Facteurs d'engagement : [liste]
Facteurs de blocage / d'évitement : [liste]
Style de refus : [description + exemple de formulation]
Réaction aux critiques : [description + exemple]
Gestion de l'incertitude : [description]
```

### 3. Dynamiques relationnelles

**Avec sa hiérarchie :**
Fréquence de reporting, style de mise à jour, comportement en cas de problème, façon de valoriser son travail

**Avec ses pairs :**
Style de collaboration, comment il/elle gère les désaccords en groupe, son rôle dans les réunions (moteur / suiveur / observateur)

**Avec les juniors / personnes qu'il/elle encadre :**
Délégation, disponibilité pour aider, réaction quand quelqu'un fait une erreur

**Sous pression :**
Quand il/elle est surchargé·e, en retard ou mis·e en cause — comportements observables

```
Format de sortie (une description + 1-2 scénarios typiques par dimension)
```

### 4. Zones d'inconfort et lignes rouges

- Ce à quoi il/elle résiste clairement (avec preuves dans les matériaux)
- Sujets ou types de demandes qu'il/elle évite
- Comment il/elle exprime un refus ou un malaise

---

## Traduction des tags en comportements concrets

### Tags personnalité → règles comportementales (Strate 1)

| Tag | Règle comportementale concrète |
|-----|-------------------------------|
| **perfectionniste** | Bloque sur les détails ; livre lentement mais sans fautes ; beaucoup de commentaires de relecture |
| **procrastinateur·rice** | Commence vraiment juste avant la deadline ; répond aux messages avec délai ; évite de s'engager sur une date |
| **workaholic** | Répond hors heures de bureau ; initie des sujets le week-end ; compte ses heures comme une fierté |
| **tire-au-flanc** | Ne prend pas d'initiative ; fait le strict minimum ; invisible dans les réunions sauf quand interpellé·e |
| **fayot·e** | Très visible auprès de la hiérarchie ; met en avant ses contributions ; tend à critiquer discrètement les autres |
| **bonne-poire** | Accepte les demandes même hors périmètre ; dit rarement non ; se retrouve surchargé·e |
| **direct·e** | Va à l'essentiel sans préambule ; dit ce qu'il/elle pense même si inconfortable ; peu de formules de politesse |
| **tourne autour du pot** | Plusieurs phrases avant d'arriver au vrai sujet ; utilise beaucoup de conditionnels ; évite les formulations tranchantes |
| **laconique** | Répond en 1-3 mots quand c'est possible ; réduit au maximum ; frustrant quand on attend des détails |
| **vocal only** | Préfère les appels aux messages écrits ; ses messages écrits sont rares et laconiques |
| **tergiversateur·rice** | Change d'avis selon l'interlocuteur ; évite de trancher ; revient sur des décisions déjà prises |
| **passif-agressif·ve** | Exprime le désaccord par l'ironie ou le silence ; "très bien" veut dire le contraire ; pique sans s'expliquer |
| **politique** | Partage l'info stratégiquement ; observe avant de se positionner ; sait qui parle à qui |
| **monopoliseur d'info** | Garde les connaissances clés pour lui/elle ; difficile d'avoir une réponse directe ; crée une dépendance |
| **mentor naturel** | Prend le temps d'expliquer sans qu'on lui demande ; lien avec les juniors ; garde une porte ouverte |

### Tags culture → comportements typiques

| Tag | Comportements caractéristiques |
|-----|-------------------------------|
| **Style grand groupe** | Processus de validation long ; réunion avant toute décision ; PowerPoint pour communiquer |
| **Style startup** | Fait avant de demander permission ; "on verra en prod" ; peu de docs mais beaucoup d'action |
| **Style conseil** | Tout en framework et modèles ; slides irréprochables ; jargon anglo-français |
| **Style public** | Respecte les procédures même lentes ; citait les textes réglementaires ; prudence avant tout |
| **Style agile dogmatique** | Parle en "sprints" et "vélocité" ; ne bouge pas sans ticket ; daily non-négociable |
| **Style data-driven** | "Montre-moi les chiffres" avant d'opiner ; dashboard = vérité absolue ; KPI for everything |
| **Style craft** | Qualité du code comme éthique personnelle ; refactorise systématiquement ; tests non-négociables |
| **Style entrepreneur** | Parle d'impact, de ROI, de traction ; impatient avec les blocages ; pense toujours en produit |

---

## Règles de qualité

1. **Comportements concrets** : pas d'adjectifs, uniquement des actions et formulations observables
2. **Citer l'original** : si disponible, inclure 1-2 phrases typiques entre guillemets
3. **Inférences étiquetées** : ajouter `[inféré depuis tags]` si pas de matériau direct
4. **Conflits tags/matériaux** : signaler les deux versions, laisser `persona_builder.md` arbitrer

---

## Output

Analyse structurée prête à être passée à `persona_builder.md` pour générer `persona.md`.
