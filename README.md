# 🐛 Bugs C Subtils

> **Collection exhaustive des pièges les plus vicieux en programmation C et systèmes embarqués**

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen)](https://s-celles.github.io/bugs-c-subtils/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Made with ❤️](https://img.shields.io/badge/Made%20with-❤️-red.svg)]()

---

## 🎯 **Aperçu**

Ce repository contient une **collection soigneusement documentée** des bugs les plus subtils et dangereux en programmation C, particulièrement dans le contexte des **systèmes embarqués**. Chaque bug est présenté avec :

- 🔍 **Exemples concrets** reproduisant le problème
- ⚠️ **Niveau de criticité** et impact potentiel
- ✅ **Solutions pratiques** et bonnes pratiques
- 🎓 **Explications pédagogiques** détaillées

## 📊 **Statistiques**

| Métrique | Valeur |
|----------|--------|
| **🐛 Types de bugs documentés** | 15+ |
| **🔥 Niveau de criticité** | Critique à Élevé |
| **⏰ Temps de debug typique** | Heures à jours |
| **💀 Impact potentiel** | Système figé à failles de sécurité |
| **🎯 Public cible** | Étudiants, développeurs C/embarqué |

---

## 🚀 **Accès Rapide**

### 📖 **Documentation en Ligne**
👉 **[Visitez le site web](https://s-celles.github.io/bugs-c-subtils/)** pour une expérience de lecture optimale

### 📋 **Table des Matières**

1. **[Collection Complète](docs/subtle_c_bugs_collection.html)** - Le bestiaire complet des bugs subtils
2. **[Guide uint8_t Loop Bug](docs/unsigned_loop_bug_presentation.html)** - Focus sur le piège classique des boucles

---

## 🎓 **Contenu Pédagogique**

### 🔢 **Bugs Arithmétiques et de Débordement**
- **Débordement d'entiers silencieux** ⚠️ CRITIQUE
- **Comparaisons signées/non signées** 
- **Promotion d'entiers surprise**

### 🎭 **Bugs de Types et Conversions**
- **Casting dangereux de pointeurs**
- **Alignement mémoire incorrect**
- **Endianness et portabilité**

### 🔄 **Bugs de Contrôle de Flux**
- **Boucles infinies avec types non signés**
- **Conditions de course**
- **Gestion d'erreurs défaillante**

### 💾 **Bugs Mémoire**
- **Buffer overflow classique**
- **Corruption de pile**
- **Fuites mémoire subtiles**

---

## 🛠️ **Structure du Repository**

```
bugs-c-subtils/
├── 📄 README.md                      # Ce fichier
├── 📄 LICENSE                        # Licence MIT
├── 📁 docs/                          # Documentation web
│   ├── 🌐 index.html                 # Page d'accueil
│   ├── 📊 subtle_c_bugs_collection.html
│   └── 🔄 unsigned_loop_bug_presentation.html
├── 📝 subtle_c_bugs_collection.md    # Source Markdown
└── 📝 uint8_loop_bug_guide.md        # Guide simplifié
```

---

## 🎯 **Public Cible**

### 👨‍🎓 **Étudiants**
- **Informatique, Informatique industrielle, Électronique**
- Apprentissage des pièges du langage C
- Préparation aux projets embarqués

### 👨‍💻 **Développeurs**
- **C/C++ embarqué, firmware**
- Révision des bonnes pratiques
- Debug et résolution de problèmes

### 👨‍🏫 **Enseignants**
- **Ressource pédagogique prête à l'emploi**
- Exemples concrets pour cours
- Support de TP et projets

---

## 🚨 **Bugs Emblématiques**

### 🔄 **Le Piège uint8_t Loop**
```c
// ❌ DANGER : Boucle infinie !
for (uint8_t i = 15; i >= 0; i--) {
    // Ce code ne termine jamais...
}
```
**Pourquoi ?** `uint8_t` ne peut pas être négatif, donc `i >= 0` est toujours vrai !

### 💥 **Débordement Silencieux**
```c
// ❌ DANGER : Calcul faux
uint8_t temp = 200;  // 200°C
uint8_t offset = 100; // +100°C
uint8_t result = temp + offset;  // 300 → 44 !
```
**Impact :** Décisions critiques basées sur des valeurs erronées.

---

## 📚 **Utilisation**

### 🌐 **Navigation Web**
1. Visitez [s-celles.github.io/bugs-c-subtils](https://s-celles.github.io/bugs-c-subtils/)
2. Choisissez votre parcours :
   - **Collection complète** pour une vue exhaustive
   - **Guide uint8_t** pour un focus spécifique

### 📖 **Lecture Locale**
```bash
# Cloner le repository
git clone https://github.com/s-celles/bugs-c-subtils.git

# Ouvrir les fichiers Markdown
cd bugs-c-subtils
# Lire avec votre éditeur préféré
```

---

## 🤝 **Contribution**

Les contributions sont les bienvenues ! Vous pouvez :

- 🐛 **Signaler de nouveaux bugs** via les Issues
- 📝 **Proposer des améliorations** via les Pull Requests
- 💡 **Suggérer des exemples** pédagogiques
- 🔍 **Corriger des erreurs** ou typos

### 📋 **Guidelines**
1. **Format cohérent** : Suivez la structure existante
2. **Exemples testés** : Code reproduisant réellement le bug
3. **Solutions pratiques** : Proposez toujours des alternatives
4. **Documentation claire** : Expliquez le "pourquoi" pas seulement le "comment"

---

## 📄 **Licence**

Ce projet est sous licence **MIT** - voir le fichier [LICENSE](LICENSE) pour plus de détails.

---

## 🎓 **Contexte Éducatif**

### 🎯 **Objectifs Pédagogiques**
- ✅ Sensibilisation aux pièges du langage C
- ✅ Développement de réflexes de programmation sûre
- ✅ Amélioration des compétences de debugging
- ✅ Préparation aux projets industriels

---

## 📞 **Contact & Support**

- 🐛 **Bugs/Issues** : [GitHub Issues](https://github.com/s-celles/bugs-c-subtils/issues)
- 💬 **Discussions** : [GitHub Discussions](https://github.com/s-celles/bugs-c-subtils/discussions)
- 📧 **Contact direct** : Voir le profil GitHub

---

## ⭐ **Remerciements**

Merci à tous ceux qui contribuent à rendre la programmation C plus sûre et accessible !

**Si ce repository vous aide, n'hésitez pas à lui donner une ⭐ !**

---

<div align="center">

**🎓 Fait avec ❤️ pour l'éducation et la prévention des bugs critiques**

[🌐 Site Web](https://s-celles.github.io/bugs-c-subtils/) • [📝 Documentation](docs/) • [🐛 Issues](https://github.com/s-celles/bugs-c-subtils/issues)

</div>
