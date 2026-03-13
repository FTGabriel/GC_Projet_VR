# GC_Projet_VR

## Prérequis
Version Unreal : 5.6.1

Casque VR : Meta 3s ou équivalent

Intégration VR Meta sur unreal : https://developers.meta.com/horizon/downloads/package/unreal-engine-5-integration/81.0/

## Table of Contents
1.  [Rayane](#1-Rayane)
2.  [Gabriel](#2-Gabriel)
3.  [Jonathan](#3-Jonathan)
4.  [Jacqueline](#4-Jacqueline)
5.  [Nathan](#5-Nathan)

---
## 1. Rayane
### 1.1 Identité Mini-jeu
### 1.2. Règle du mini-jeu
### 1.3 Architecture Technique
---
## 2. Gabriel
### 2.1 Identité Mini-jeu
### 2.2. Règle du mini-jeu
### 2.3 Architecture Technique
---
## 3. Jonathan
### 3.1 Identité Mini-jeu
### 3.2. Règle du mini-jeu
### 3.3 Architecture Technique
---
## 4. Jacqueline
### 4.1 Identité Mini-jeu
Nom : Salle de réflexe

Niveau : Très facile

Où le trouver dans le hub : Facile, c'est marqué Reflex room au dessus et c'est le seul où on peut voir des cubes rouge et bleu apparaitre et disparaitre !

### 4.2. Règle du mini-jeu

Vous êtes là pour développer et améliorer vos réflexes. Ici, vous allez devoir esquiver et taper les objets qui arrivent.

Cube bleu : Tapez les avec vos mains

Cube rouge : Évitez les avec votre tête

### 4.3 Architecture Technique
Système de Collision : Utilisation d'Overlap Events avec détection par Actor Tags (Target pour BP_Target et Avoid pour BP_Avoid).

Communication : Utilisation de Casts pour la mise à jour du score entre les actions du pawn et le Widget, affichant le score.

Game Feel : Intégration de feedbacks visuels via des particules (ici explosion) à l'impact (ps: je n'ai pas intégré la haptique car je n'aime pas les vibrations dans les manettes).

---
## 5. Nathan
### 5.1 Identité Mini-jeu
### 5.2. Règle du mini-jeu
### 5.3 Architecture Technique
---
