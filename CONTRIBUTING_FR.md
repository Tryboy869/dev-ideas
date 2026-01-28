# Contribuer à /dev/ideas

Merci de votre intérêt pour contribuer ! Ce document explique comment soumettre des idées, ce qui fait une bonne soumission, et le processus de révision.

---

## 📋 Démarrage rapide

**Soumettre une idée en 4 étapes :**

1. **Forkez** ce dépôt
2. **Créez** un fichier JSON dans `ideas/votre-idee-slug.json`
3. **Suivez** la structure définie dans [`schema/idea.schema.json`](schema/idea.schema.json)
4. **Ouvrez** une Pull Request

**Notre validation automatique vérifiera votre soumission**, et un mainteneur examinera le contenu.

---

## ✅ Qu'est-ce qu'une bonne idée ?

### Principe fondamental
> **"Toute idée est valide tant qu'elle est cohérente."**

Une idée n'a pas besoin d'être :
- ✗ Déjà implémentée
- ✗ Commercialement viable
- ✗ Rigoureuse académiquement

Mais elle **doit** avoir :
- ✓ Un problème technique clair
- ✓ Une approche ou intuition identifiable
- ✓ Une preuve que ce n'est pas absurde (contraintes, cas limites, ou références)

---

## 📝 Structure JSON

### Champs obligatoires

```json
{
  "id": "slug-unique-ici",
  "title": "Titre concis de votre idée",
  "category": "distributed-systems",
  "status": "hypothesis",
  "author": {
    "github": "votre-username",
    "doi": null
  },
  "content": {
    "problem": "Quel problème technique cela résout-il ? (20-500 caractères)",
    "approach": "Intuition ou méthode de haut niveau (20-500 caractères)",
    "why_not_bullshit": "Pourquoi c'est techniquement cohérent (20-500 caractères)"
  },
  "metadata": {
    "created": "2026-01-24",
    "updated": "2026-01-24",
    "tags": ["tag1", "tag2", "tag3"]
  }
}
```

### Optionnel : Preuves (obligatoires pour les statuts `poc` ou `validated`)

Si votre idée a atteint le stade **PoC** ou **Validated**, vous **devez** inclure des preuves :

```json
{
  ...
  "status": "poc",
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
}
```

**Types de preuves acceptés :**
- `github` / `gitlab` — Code source
- `colab` / `jupyter` — Notebooks interactifs
- `video` — YouTube, Vimeo, Loom (démos de 3-10 min)
- `demo` — Sites live (Vercel, Netlify, etc.)
- `paper` — arXiv, DOI, ou PDF hébergé

**Limite : 3 preuves maximum**

---

## 🔄 Cycle de vie d'une idée

Votre idée évoluera à travers ces étapes :

| Statut | Description | Exigences |
|--------|-------------|-----------|
| **hypothesis** | Intuition non testée | Seulement les 3 champs de contenu de base |
| **experimentation** | Tests actifs | Mentionner les données expérimentales dans `why_not_bullshit` |
| **concept** | Approche structurée | Documenter l'architecture ou le design |
| **poc** | Prototype fonctionnel | **Au moins 1 preuve requise** |
| **validated** | Reproduit par d'autres | **Multiples implémentations citées** |

Vous pouvez mettre à jour le statut de votre idée en soumettant une nouvelle PR qui modifie votre fichier JSON.

---

## 🎯 Catégories

Choisissez la catégorie **principale** qui correspond le mieux à votre idée :

- `distributed-systems`
- `ai`
- `programming-languages`
- `developer-tools`
- `security`
- `networking`
- `databases`
- `hardware`
- `meta-programming`
- `other`

---

## 🚀 Processus de soumission

### Étape 1 : Créer votre fichier JSON

```bash
# Cloner votre fork
git clone https://github.com/VOTRE-USERNAME/ideas.git
cd ideas

# Créer votre fichier d'idée
cp ideas/distributed-sqlite-crdt.json ideas/mon-idee-geniale.json

# Éditez-le avec votre contenu
nano ideas/mon-idee-geniale.json
```

### Étape 2 : Valider localement (Optionnel)

```bash
# Installer ajv-cli
npm install -g ajv-cli ajv-formats

# Valider votre JSON
ajv validate -s schema/idea.schema.json -d ideas/mon-idee-geniale.json
```

### Étape 3 : Ouvrir une Pull Request

```bash
git add ideas/mon-idee-geniale.json
git commit -m "feat: ajouter l'idée pour [Votre Titre]"
git push origin main
```

Puis ouvrez une PR sur GitHub. Nos vérifications automatiques s'exécuteront.

---

## 🤖 Validation automatique

Lorsque vous ouvrez une PR, GitHub Actions va :

1. ✅ Valider la structure JSON contre le schéma
2. ✅ Vérifier les IDs dupliqués
3. ✅ Vérifier que le statut `poc`/`validated` a des preuves
4. ✅ Auto-labelliser votre PR si toutes les vérifications passent

Si la validation échoue, consultez les messages d'erreur et mettez à jour votre PR.

---

## 👥 Processus de révision

**Après la validation automatique :**

1. Un mainteneur examinera le **contenu** de votre idée (pas seulement la structure)
2. Il pourra poser des questions ou suggérer des améliorations via les commentaires de la PR
3. Une fois approuvée, votre PR sera fusionnée
4. **Une Discussion GitHub sera créée automatiquement** pour votre idée

---

## 📜 Code de conduite

Nous appliquons une politique de **tolérance zéro** pour :

- ❌ Attaques personnelles ou harcèlement
- ❌ Commentaires condescendants ou toxiques
- ❌ Trolling ou arguments de mauvaise foi

**Les contrevenants seront avertis une fois, puis bannis.**

### Notre standard

- ✅ Critiquer les **idées**, jamais les **personnes**
- ✅ Présumer la bonne foi
- ✅ Être constructif et bienveillant

---

## 🎓 Attribution académique

Si vous souhaitez que votre idée soit citable :

1. Téléversez votre document d'idée sur [Zenodo](https://zenodo.org) ou [HAL](https://hal.science)
2. Obtenez un DOI
3. Ajoutez-le au champ `author.doi` de votre idée

Les idées avec DOI recevront un badge 🎓 sur le site web.

---

## 🔗 Lien vers les Discussions

Une fois votre idée fusionnée, une Discussion GitHub sera créée. Vous pouvez :

- Partager l'URL de la discussion sur les réseaux sociaux
- Y faire référence dans des articles de blog ou papers
- Inviter des collaborateurs à discuter là-bas

---

## 🙋 Besoin d'aide ?

- **Questions sur la soumission ?** [Ouvrir une Discussion](https://github.com/Tryboy869/ideas/discussions)
- **Trouvé un bug dans le site ou l'automatisation ?** [Ouvrir une Issue](https://github.com/Tryboy869/ideas/issues)
- **Vous voulez devenir mainteneur ?** Contribuez régulièrement pendant 3+ mois, puis contactez [@anzize](https://github.com/anzize)

---

**Merci de contribuer à /dev/ideas !** 🚀