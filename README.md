# TP2 – Application Web JSF avec PrimeFaces et LangChain4j (Gemini)
BENDAHOU SAAD -8-G2 -

## 📌 Description
Ce projet correspond au **TP2** du module Jakarta EE.  
Il s’agit de créer une **application Web JSF** qui permet d’interagir avec un modèle de langage (LLM – Gemini) en utilisant **LangChain4j**.  
L’application reprend l’interface utilisateur des TP précédents (TP0 et TP1), sans le mode debug, et ajoute une intégration avec un LLM via une classe métier dédiée (`LlmClient`).

---

## 🏗️ Structure du projet
- **Page JSF** : `index.xhtml`  
  - Interface utilisateur de type chat.  
  - Liens vers les fichiers CSS et JavaScript situés dans `src/main/webapp/resources/css` et `src/main/webapp/resources/js`.

- **Ressources statiques** :  
  - `resources/css/mycsslayout.css`  
  - `resources/js/script.js`

- **Backing bean** :  
  - Portée : `@ViewScoped`  
  - Responsable de la logique de conversation avec l’utilisateur.  
  - Délègue la requête au `LlmClient`.

- **Classe métier (LlmClient)** :  
  - Gère la communication avec Gemini via **LangChain4j**.  
  - Utilise un **ChatMemory** pour conserver l’historique des échanges.  
  - Configure l’interface `Assistant` (service IA) pour poser des questions et recevoir des réponses.  

