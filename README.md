# GC_Projet_VR

## Prérequis
Version Unreal : 5.6.1

Casque VR : Meta 3s ou équivalent

Intégration VR Meta sur unreal : https://developers.meta.com/horizon/downloads/package/unreal-engine-5-integration/81.0/

## Sommaire
1.  [Rayane](#1-rayane)
2.  [Gabriel](#2-gabriel)
3.  [Jonathan](#3-jonathan)
4.  [Jacqueline](#4-jacqueline)
5.  [Nathan](#5-nathan)

---
## 1. Rayane
### 1.1 Identité Mini-jeu
### 1.2. Règle du mini-jeu
### 1.3 Architecture Technique
### 1.4 Difficulté(s) rencontré(s)
---
## 2. Gabriel
### 2.1 Identité Mini-jeu
### 2.2. Règle du mini-jeu
### 2.3 Architecture Technique
### 2.4 Difficulté(s) rencontré(s)
---
## 3. Jonathan
### 3.1 Identité Mini-jeu
### 3.2. Règle du mini-jeu
### 3.3 Architecture Technique
### 3.4 Difficulté(s) rencontré(s)
---
## 4. Jacqueline

---
### 4.1 Identité Mini-jeu
Nom : Salle de réflexe

Niveau : Facile

Où le trouver dans le hub : Facile, c'est marqué Reflex room au dessus. C'est le seul où l'on peut voir des cubes rouges et bleus apparaître et disparaître !

En cas de problème avec Main ou Dev pour ma partie : Testez sur la branche Lynn

---
### 4.2. Règle du mini-jeu

Vous êtes là pour développer et améliorer vos réflexes. Ici, vous allez devoir esquiver et taper les objets qui arrivent.

Cube bleu : Tapez-les avec vos mains.

Cube rouge : Évitez les avec votre tête.

Cube violet : Tapez-les ou évitez les. (Attention, celui là est plus rapide afin de tester votre réflexe)

---
### 4.3 Architecture Technique

Système de Collision : Utilisation d'Overlap Events avec détection par Actor Tags (Target pour BP_Target et Avoid pour BP_Avoid).

Communication : Utilisation de Casts pour la mise à jour du score entre les actions du pawn et le Widget, affichant le score.

Game Feel : Intégration de feedbacks visuels via des particules (ici une explosion) à l'impact (PS : je n'ai pas intégré l'haptique car je n'apprécie pas les vibrations dans les manettes).

---
### 4.4 Difficultés rencontrés
- La prise en main du casque : N'ayant jamais utilisé de casque VR, j'ai eu la difficulté de trouver comment régler les lentilles ainsi que la connection du casque à Unreal.
  
- Les configurations matérielles : Mon ordinateur personnel n'ayant pas une carte graphique assez puissante (mémoire vidéo insuffisante), j'ai dû travailler sur les postes de l'école. La disponibilité des salles et l'état des machines (Bitlocker, GPU incompatibles, PC défectueux) ont représenté un défi supplémentaire..
  
- L'organisation de l'école : La préparation tardive du matériel VR dans les salles et le manque de casques par rapport au nombre d'élèves ont rendu le développement complexe et frustrant..

---
## 5. Nathan

### 5.1 Identité Mini-jeu

Nom du projet : The Rotating Bar
Niveau : Moyen
Concept : Un jeu d'adresse et de tri où le joueur doit placer des bouteilles dans les tuyaux correspondants tout en gérant un environnement en mouvement constant.
Ambiance : Arcade, dynamique et immersive.

### 5.2. Règle du mini-jeu

Activation : Le jeu démarre lorsque le joueur entre dans la zone centrale du comptoir.
Objectif : Attraper les bouteilles qui spawnent sur le comptoir tournant et les insérer dans les tuyaux de la couleur correspondante.
Haptique : Une validation réussie déclenche une vibration dans les contrôleurs et un son pour confirmer le point.
Évolution : Toutes les 15 secondes, la vitesse de rotation du comptoir et de la salle entière augmente, rendant le tri de plus en plus difficile.
Pause Dynamique : Si le joueur quitte le centre du comptoir, la rotation ralentit progressivement jusqu'à l'arrêt total pour mettre le jeu en pause.
Nettoyage : Toute bouteille tombant hors de la scène est automatiquement détruite par une Kill Zone pour optimiser les performances.

### 5.3 Architecture Technique

Le projet repose sur une architecture modulaire et optimisée :
- Actor Component (BPC_RotationManager) : Un composant universel qui gère l'accélération et la décélération fluide (FInterp To) de n'importe quel objet possédant un RotatingMovementComponent.
- Système d'Attachement Dynamique : Utilisation de AttachActorToComponent avec gestion des collisions (Set Actor Enable Collision) pour souder les bouteilles au comptoir tournant dès leur apparition.
- Gestion des Événements : Utilisation de Timers pour l'accélération par paliers et de Tick optimisé (avec branches de condition) pour les transitions de vitesse fluides.
- Hiérarchie de Scène : Fusion d'objets via un Blueprint de scène (BP_Scene) pour permettre une rotation complexe de l'environnement complet.

### 5.4 Difficulté(s) rencontré(s)

- Conflits de Physique au Spawn : Résolu en désactivant temporairement les collisions de l'acteur lors du spawn pour permettre un attachement propre sans explosion physique du moteur.
- Héritage de Logique : Transition d'une logique codée "en dur" dans chaque objet vers un Actor Component réutilisable, permettant de piloter simultanément le comptoir et la salle avec le même code.
- Immersion VR & Confort : Mise en place d'interpolations de vitesse (FInterp To) pour éviter les démarrages et arrêts brusques, minimisant ainsi les risques de cinétose (motion sickness) en VR.
- Synchronisation des sous-niveaux : Communication entre le trigger du comptoir et le Blueprint de la scène pour assurer un départ synchronisé de tous les éléments mobiles.

---
