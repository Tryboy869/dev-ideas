# /dev/ideas

> **Le registre ouvert pour les idées techniques proof-of-concept**

[![Site Web](https://img.shields.io/badge/site-en_ligne-brightgreen)](https://tryboy869.github.io/ideas/)
[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-blue.svg)](LICENSE.md)
[![GitHub Discussions](https://img.shields.io/github/discussions/Tryboy869/ideas)](https://github.com/Tryboy869/ideas/discussions)

**Fondé par [Daouda Abdoul Anzize](https://github.com/anzize) — Janvier 2026**

Designer de Paradigmes Computationnels • 40+ projets open-source  
[Portfolio](https://tryboy869.github.io/daa) • [Twitter/X](https://twitter.com/Nexusstudio100) • [LinkedIn](https://linkedin.com/in/anzize-adéléké-daouda)

---

## 🎯 Pourquoi ce projet existe

L'écart entre **"J'ai une idée"** et **"Voici un prototype fonctionnel"** tue l'innovation.

- Les articles académiques sont trop lents
- Les repos GitHub sans contexte sont invisibles
- Les threads Twitter disparaissent
- Les notes privées ne sont jamais validées

**`/dev/ideas` est la couche manquante** — où la cohérence technique compte plus que les diplômes.

---

## 🚀 Comment ça marche

```
1. Soumettre → Fichier JSON via Pull Request
2. Valider → Vérification automatique de la structure
3. Discuter → Une Discussion GitHub s'ouvre automatiquement
4. Évoluer → Hypothèse → Expérimentation → Concept → PoC → Validé
```

**Votre idée. Notre validation collective.**

---

## 📊 Statut actuel

- 🌱 **Tout juste lancé** (Janvier 2026)
- 💡 10 idées initiales pour démontrer le format
- 🔨 Recherche active de contributeurs

**[Explorer le catalogue →](https://tryboy869.github.io/ideas/)**

---

## 🛠️ Cycle de vie d'une idée

| Phase | Description | Exemple |
|-------|-------------|---------|
| **Hypothesis** | Intuition non testée | "Et si SQLite utilisait des CRDTs ?" |
| **Experimentation** | Tests actifs, collecte de données | "Prototype basique construit, 20% d'overhead observé" |
| **Concept** | Approche structurée | "Architecture de la couche CRDT documentée" |
| **PoC** | Prototype fonctionnel | "Repo de démo avec benchmarks" |
| **Validated** | Reproduit par d'autres | "3+ implémentations indépendantes" |

---

## 📝 Comment contribuer

**Lisez le guide complet :** [CONTRIBUTING.md](CONTRIBUTING.md) | [CONTRIBUTING_FR.md](CONTRIBUTING_FR.md)

**Démarrage rapide :**
1. Forkez ce repo
2. Créez `ideas/votre-idee-slug.json` en suivant le [schéma](schema/idea.schema.json)
3. Ouvrez une Pull Request
4. La validation automatique s'exécute
5. Si approuvé, un thread de Discussion est créé automatiquement

---

## 🔗 Preuves de concept (PoC)

Pour les idées au stade **PoC** ou **Validated**, vous **devez** fournir des preuves :

**Types acceptés (max 3) :**
- 🐙 **Code source** : GitHub, GitLab
- 📓 **Notebooks** : Jupyter, Google Colab
- 🎥 **Vidéo** : YouTube, Vimeo, Loom (démo de 3-10 min)
- 🌐 **Site démo** : Vercel, Netlify, Heroku
- 📄 **Paper** : arXiv, DOI, PDF hébergé

**Exemple dans le JSON :**
```json
"proofs": [
  {
    "type": "github",
    "url": "https://github.com/user/repo",
    "description": "Prototype fonctionnel avec benchmarks"
  },
  {
    "type": "video",
    "url": "https://youtube.com/watch?v=...",
    "description": "Démo de 5 minutes"
  }
]
```

---

## 📂 Structure du dépôt

```
/dev/ideas/
├── .github/
│   └── workflows/
│       ├── validate-idea.yml      # Valide la structure JSON
│       ├── create-discussion.yml  # Crée automatiquement une Discussion
│       └── build-site.yml         # Génère le site statique
├── ideas/
│   ├── distributed-sqlite-crdt.json
│   ├── neural-kernel-scheduler.json
│   └── ...
├── schema/
│   └── idea.schema.json           # Schéma JSON pour validation
├── docs/
│   ├── index.html                 # Site web généré
│   └── ideas.json                 # Auto-généré depuis ideas/*.json
├── README.md                       # Documentation anglaise
├── README_FR.md                    # Documentation française
├── CONTRIBUTING.md                 # Guide de contribution anglais
├── CONTRIBUTING_FR.md              # Guide de contribution français
├── LICENSE.md
└── CODE_OF_CONDUCT.md
```

---

## 🎓 Idées en vedette

- **[NEXUS AXION](ideas/nexus-axion-paradigm-absorption.json)** — Framework computationnel universel par absorption de paradigmes
- **[Neural Kernel Scheduler](ideas/neural-kernel-scheduler.json)** — Remplacer CFS par un ordonnanceur LSTM
- **[Self-Healing WASM](ideas/self-healing-wasm.json)** — Rollback automatique sur erreur runtime

**[Voir toutes les idées →](https://tryboy869.github.io/ideas/)**

---

## 🤝 Gouvernance

- **Mainteneur fondateur** : [Daouda A. Anzize](https://github.com/anzize)
- **Licence** : CC BY-SA 4.0 (idées), MIT (code/scripts)
- **Décisions** : Consensus communautaire via Discussions
- **Rotation des mainteneurs** : Nouveaux co-mainteneurs tous les 6 mois

**Ceci est un projet communautaire.** Le rôle du fondateur est de superviser, pas de contrôler.

---

## 📜 Licence

- **Idées, descriptions, documentation** : [CC BY-SA 4.0](LICENSE.md)
- **Snippets de code, scripts** : [MIT](LICENSE.md)

---

## 🌟 Reconnaissance

Si vous utilisez une idée de ce registre dans votre travail :
- **Citation académique** : Utilisez le DOI fourni (si disponible)
- **Attribution informelle** : Lien vers le thread de Discussion de l'idée
- **Star ce repo** pour montrer votre soutien

---

## 📬 Contact

**Questions ? Suggestions ?**
- Ouvrez une [Discussion](https://github.com/Tryboy869/ideas/discussions)
- Contactez [@anzize](https://github.com/anzize)
- Email : contact@proton.me

---

**Construit avec ❤️ par la communauté technique.**