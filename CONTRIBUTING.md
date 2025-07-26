# Contribuer à Food & Drinks Ratings (FDR)

Merci de votre intérêt pour contribuer à **FDR** ! Ce document décrit les étapes pour participer au projet.

---

## 🚀 Comment contribuer ?

1. **Forker** le dépôt GitHub.
2. **Cloner** votre fork :
   ```bash
   git clone https://github.com/votre-compte/fdr.git
   cd fdr
   ```
3. **Créer une branche** pour votre fonctionnalité ou correction :
   ```bash
   git checkout -b feature/ma-fonctionnalite
   ```
4. **Coder** votre modification (voir [Bonnes pratiques](#bonnes-pratiques)).
5. **Lancer les tests & le lint** :
   ```bash
   npm run lint
   npm test
   ```
6. **Commit & push** :
   ```bash
   git commit -m "feat: ajouter ma fonctionnalité"
   git push origin feature/ma-fonctionnalite
   ```
7. **Créer une Pull Request** sur GitHub.

---

## 📝 Bonnes pratiques

- **Conventional Commits** : utilisez les préfixes `feat:`, `fix:`, `docs:`, `style:`, etc.
- **Lint & formatage** : exécutez `npm run lint` avant de pousser vos commits.
- **Typescript** : vérifiez que le typage reste correct.
- **Tests** : si possible, ajoutez des tests unitaires.

---

## 🧑‍🤝‍🧑 Issues & Discussions

- Les tickets faciles sont étiquetés **good first issue**.
- Les suggestions d'amélioration sont les bienvenues via **Issues** ou **Discussions**.

---

## 📄 Licence

En contribuant, vous acceptez que votre code soit publié sous la [Licence MIT](LICENSE).
