Pour insaller : npm install @HummusFriendly/react-modal

Tu l’importes dans ton composant, tu gères un useState pour savoir si la modale est ouverte ou pas, et c’est tout. Exemple :

import React, { useState } from 'react';
import Modal from '@votre-username/react-modal';

function App() {
  const [isOpen, setIsOpen] = useState(false);

  return (
    <div>
      <button onClick={() => setIsOpen(true)}>Ouvrir la modale</button>
      <Modal isOpen={isOpen} onClose={() => setIsOpen(false)}>
        <p>Contenu de la modale</p>
      </Modal>
    </div>
  );
}

isOpen : (obligatoire) si tu veux que la modale soit affichée, tu mets true.

onClose : (obligatoire aussi) fonction pour fermer la modale (quand tu cliques à l’extérieur ou sur un bouton “Fermer”).

children : (toujours obligatoire) c’est le contenu que tu veux mettre dedans (texte, formulaire, bouton, gif de chaton, etc.).

PS: Tailwind CSS pour le style (cf la doc pour l'installer) + Version React 16.8 ou plus. 
