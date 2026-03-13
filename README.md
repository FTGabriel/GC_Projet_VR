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
### 5.2. Règle du mini-jeu
### 5.3 Architecture Technique
### 5.4 Difficulté(s) rencontré(s)
---
