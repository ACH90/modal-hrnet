# hrnet-modal (FR)

Un composant **React** léger, accessible et sans dépendances externes pour afficher une **modale personnalisée** dans vos projets.

## ✨ Fonctionnalités

- **Accessibilité** : rôle ARIA, focus piégé dans la modale, fermeture au clavier (`Escape`)
- **Design personnalisable** : styles CSS modulaires
- **Empêche le scroll** de l’arrière-plan lors de l’ouverture
- **Interaction naturelle** : clic en dehors pour fermer, bouton de fermeture

---

## 📦 Installation

```bash
npm i @ach90/hrnet-modal
```

## 🧑‍💻 Utilisation de base

``` javascript
import React, { useState } from "react";
import Modal from "hrnet-modal";
import "hrnet-modal/dist/style.css"; // N'oubliez pas d'importer les styles !

function App() {
  const [isOpen, setIsOpen] = useState(false);

  return (
    <>
      <button onClick={() => setIsOpen(true)}>Ouvrir la modale</button>

      <Modal isOpen={isOpen} onClose={() => setIsOpen(false)}>
        <h2>Bienvenue !</h2>
        <p>Ceci est le contenu de votre modale.</p>
        <button onClick={() => setIsOpen(false)}>Fermer</button>
      </Modal>
    </>
  );
}
```

## 🧩 Props 

Prop	    Type	    Description
isOpen	    boolean	    Contrôle si la modale est affichée (true) ou non (false)
onClose	    function	Fonction appelée quand la modale doit être fermée (clic extérieur, ESC, etc.)
children	ReactNode	Contenu affiché dans la modale

## 🎨 Personnalisation des styles

Par défaut, la modale utilise des styles définis dans style.css (Modal.module.css compilé).

Pour personnaliser :

Écrase les classes CSS avec des sélecteurs spécifiques

Ou copie le composant et applique ton propre fichier CSS


-------------


# hrnet-modal (EN)

A lightweight and **accessible React modal component** with **no external dependencies**, designed to integrate easily into your projects.

## ✨ Features

- **Accessibility built-in**: ARIA roles, focus trapping, ESC key to close
- **Customizable design**: modular CSS styling
- **Prevents background scrolling** when modal is open
- **Natural interaction**: close on outside click or via close button

---

## 📦 Installation

```bash
npm i @ach90/hrnet-modal
```

## 🧑‍💻 Basic Usage

``` javascript
import React, { useState } from "react";
import Modal from "hrnet-modal";
import "hrnet-modal/dist/style.css"; // N'oubliez pas d'importer les styles !

function App() {
  const [isOpen, setIsOpen] = useState(false);

  return (
    <>
      <button onClick={() => setIsOpen(true)}>Open Modal</button>

      <Modal isOpen={isOpen} onClose={() => setIsOpen(false)}>
        <h2>Welcome!</h2>
        <p>This is the content of your modal.</p>
        <button onClick={() => setIsOpen(false)}>Close</button>
      </Modal>
    </>
  );
}
```

## 🧩 Props 

Prop	    Type	    Description
isOpen	    boolean	    Controls whether the modal is visible (true) or hidden (false)
onClose	    function	Function called when the modal should be closed (outside click, ESC, etc.)
children	ReactNode	The content to display inside the modal

## 🎨 Styling Customization

By default, the modal uses styles defined in style.css (compiled from Modal.module.css).

To customize:

Override the CSS classes with more specific selectors

Or copy the component and apply your own CSS styles