# 🎬 Batch Watermarker Studio Pro

**Batch Watermarker Studio Pro** est une application web moderne, puissante et intuitive conçue pour appliquer des filigranes (logos ou textes) en masse sur plusieurs vidéos simultanément. 

La particularité majeure de cet outil est qu'il fonctionne **100% côté client (Client-Side)**. Vos vidéos ne sont jamais téléchargées sur un serveur externe : tout le traitement (rendu, encodage et compression) est exécuté directement par la puissance de votre navigateur. Cela garantit une confidentialité absolue et une vitesse de traitement instantanée, sans aucune limite de taille de fichier liée à un hébergeur.

---

## ✨ Fonctionnalités Clés

### 🎨 Personnalisation du Filigrane
*   **Double Mode :** Choisissez entre l'importation d'un **Logo PNG transparent** ou la création d'un **Texte personnalisé** (idéal pour les mentions de copyright ou pseudos de réseaux sociaux).
*   **Contrôle Précis :** Ajustez dynamiquement l'échelle (taille) et l'opacité (transparence) du filigrane.
*   **Éditeur Visuel Interactif :** Glissez-déposez le filigrane directement sur l'aperçu vidéo pour ajuster sa position, ou utilisez les boutons d'**Ancrage Rapide** (Haut-Gauche, Centre, Bas-Droite, etc.).
*   **Mode Grille (Mosaïque) :** Activez une protection anti-vol avancée qui répète le filigrane sur toute la surface de la vidéo sous forme de motif.

### ⚡ Productivité & Pipeline de Masse (Batch)
*   **Gestion de la Liste de Lecture :** Importez plusieurs vidéos simultanément et passez de l'une à l'autre pour vérifier le rendu en temps réel.
*   **Suppression de l'Audio (Mute) :** Une option pour couper instantanément les pistes sonores de toutes les vidéos importées lors de l'export.
*   **Renommage Intelligent :** Définissez un préfixe personnalisé pour renommer automatiquement tous les fichiers exportés.
*   **Système de Presets (Sauvegarde) :** Sauvegardez vos configurations (logo, texte, opacité, options) dans la mémoire locale de votre navigateur (`localStorage`) pour les retrouver instantanément à votre prochaine visite.

### 📦 Exportation Optimisée
*   **Génération d'Archive ZIP :** Une fois le traitement terminé, l'application compile automatiquement toutes les vidéos marquées dans un fichier `.zip` téléchargeable en un clic.

---

## 🛠️ Technologies Utilisées

L'application est construite sans framework lourd afin de rester ultra-légère et portable (un seul fichier HTML) :

| Technologie / Librairie | Utilisation |
| :--- | :--- |
| **HTML5 Canvas API** | Utilisé comme moteur de rendu pour superposer les images/textes sur le flux vidéo frame par frame. |
| **MediaRecorder API** | Capture le flux du Canvas en temps réel pour encoder la nouvelle vidéo. |
| **Web Audio API** | Gère le multiplexage et l'extraction de la piste audio d'origine. |
| **Tailwind CSS** | Framework CSS pour un design d'interface moderne, épuré et adapté aux professionnels (mode sombre natif). |
| **JSZip** | Permet la création et la compression de l'archive `.zip` directement en JavaScript côté client. |
| **FontAwesome** | Bibliothèque d'icônes vectorielles pour l'interface utilisateur. |

---

## 🚀 Installation et Utilisation

L'application ne nécessite **aucune installation**, aucun serveur Node.js, ni aucune commande dans le terminal.

1. Téléchargez ou copiez le code du fichier `index.html`.
2. Double-cliquez sur le fichier `index.html` pour l'ouvrir dans votre navigateur web (Chrome, Edge, Firefox ou Safari).
3. **C'est prêt !** Vous pouvez commencer à traiter vos vidéos.

---

## 📖 Guide d'Utilisation Étape par Étape

1. **Configurer le filigrane (Panneau Gauche) :** 
   * Choisissez l'onglet **Logo PNG** ou **Texte**.
   * Importez votre image ou saisissez votre texte de marquage.
   * Ajustez la taille et l'opacité.
2. **Importer vos médias (Panneau Droit) :**
   * Cliquez sur le bouton **"Ajouter Médias"** ou glissez-déposez vos fichiers vidéos directement n'importe où sur l'écran.
3. **Ajuster le positionnement (Panneau Central) :**
   * Sélectionnez une vidéo dans la liste de droite.
   * Déplacez le logo à la souris sur l'écran ou utilisez les boutons d'ancrage rapide.
4. **Configurer les options globales :**
   * Cochez *Mode Grille* si vous souhaitez une protection totale en mosaïque.
   * Cochez *Couper le son* si nécessaire.
   * *(Optionnel)* Cliquez sur **"Sauver Preset"** pour conserver vos réglages lors de vos prochaines sessions.
5. **Exporter :** 
   * Cliquez sur le bouton **"Lancer le rendu de masse (.ZIP)"**. Une barre de progression vous indiquera l'avancement vidéo par vidéo. Le téléchargement se lancera automatiquement à 100%.

---

## ⚠️ Notes Techniques & Compatibilité

*   **Format de sortie :** Les vidéos sont exportées au format `.webm` (Codec VP9). C'est le standard de capture vidéo natif le plus performant et le mieux supporté par les navigateurs pour le rendu de Canvas en direct. Ce format est parfaitement lu par les lecteurs modernes (VLC, QuickTime) et accepté par la majorité des réseaux sociaux.
*   **Performances :** Le temps de rendu dépend directement de la puissance de votre processeur (CPU/GPU) et de la durée de vos vidéos, puisqu'elles sont lues en tâche de fond à vitesse réelle pour être ré-encodées.
