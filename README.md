# AAP Ingenia

AAP Ingenia est un prototype de back-office pour analyser des appels a projets et appels d'offres, a partir d'une base documentaire et d'un futur pipeline d'IA documentaire.

Le projet est en phase de structuration. Le dossier `contexte/` contient les notes de cadrage, les schemas de donnees et les specifications produit deja prepares. Le dossier `base de donnees appels d'offres et appels a projets vides/` contient des documents de travail et de test, laisses de cote pour l'instant dans le developpement applicatif.

## Objectif du prototype

Le prototype actuel sert a :

- centraliser la vision du projet ;
- afficher les briques du MVP ;
- preparer une premiere interface Streamlit simple ;
- poser une base propre avant l'integration de `Supabase`, `n8n` et des workflows IA.

## Structure du projet

```text
.
â”œâ”€â”€ README.md
â”œâ”€â”€ requirements.txt
â”œâ”€â”€ streamlit_app.py
â”œâ”€â”€ app/
â”‚   â”œâ”€â”€ main.py
â”‚   â”œâ”€â”€ ui/
â”‚   â”œâ”€â”€ services/
â”‚   â”œâ”€â”€ models/
â”‚   â””â”€â”€ utils/
â”œâ”€â”€ data/
â”‚   â””â”€â”€ samples/
â”œâ”€â”€ docs/
â”œâ”€â”€ contexte/
â”‚   â”œâ”€â”€ # CLAUDE.md
â”‚   â”œâ”€â”€ subly_schema_v3.sql.md
â”‚   â”œâ”€â”€ subly_point_global_projet_v3.html.html
â”‚   â””â”€â”€ ...
â””â”€â”€ base de donnees appels d'offres et appels a projets vides/
```

## Lancer le projet

1. Creer un environnement virtuel :

```bash
python3 -m venv .venv
source .venv/bin/activate
```

2. Installer les dependances :

```bash
pip install -r requirements.txt
```

3. Lancer l'application :

```bash
streamlit run streamlit_app.py
```

## Etat actuel

- vision produit : definie ;
- architecture cible : definie ;
- schema de donnees : avance ;
- application web : prototype de depart ;
- structure Python modulaire : en place ;
- automatisations et base de donnees reelles : non connectees pour l'instant.

## Prochaines etapes conseillees

1. Ajouter une page d'upload dans `app/ui/`.
2. Creer un service de lecture de documents dans `app/services/`.
3. Introduire une configuration simple pour les chemins et futures cles API.
4. Brancher ensuite `Supabase` et les workflows de traitement.
