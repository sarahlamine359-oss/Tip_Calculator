  Tip Calculator - Android Application

 📌 Description

**Tip Calculator** est une application mobile Android développée avec **Kotlin** et **Jetpack Compose**.

Cette application permet de calculer automatiquement le montant du pourboire (**Tip Amount**) à partir :
- du montant de la facture ;
- du pourcentage de pourboire choisi ;
- d'une option permettant d'arrondir le montant du pourboire.

L'application affiche ensuite le résultat du calcul.

---

## 🚀 Fonctionnalités

✅ Saisie du montant de la facture  
✅ Saisie du pourcentage de pourboire  
✅ Calcul automatique du pourboire  
✅ Option pour arrondir le pourboire  
✅ Interface moderne avec Jetpack Compose  
✅ Utilisation d'icônes pour améliorer l'expérience utilisateur  
✅ Interface adaptable aux écrans mobiles  

---

## 🛠️ Technologies utilisées

Langage :** Kotlin
 **Framework UI :** Jetpack Compose
 **IDE :** Android Studio
 **Architecture UI :** Composable Functions
 **Material Design 3**
 **State Management :**
   `remember`
   `mutableStateOf`



## 📱 Aperçu du fonctionnement

L'utilisateur :

1. Entre le montant de la facture.

Exemple :
Montant : 10000 FCFA
2. Entre le pourcentage du service.
Exemple :
Pourboire : 15 %
3. L'application calcule :
Tip Amount : 1500 FCFA
Si l'option d'arrondi est activée :
Tip Amount : 1500 FCFA

# 📂 Structure du projet

TipCalculator
│
├── app
│ ├── java
│ │ └── com.example.tipcalculator
│ │ │
│ │ └── MainActivity.kt
│ │
│ ├── res
│ │ ├── drawable
│ │ │ ├── money.xml
│ │ │ └── percent.xml
│ │ │
│ │ └── values
│ │ └── strings.xml
│ │
│ └── AndroidManifest.xml
│
└── README.md


---

# 🧮 Fonctionnement du calcul

Le calcul du pourboire est réalisé avec la fonction :

```kotlin
calculateTip()

Formule utilisée :

Pourboire = Montant de la facture × Pourcentage / 100

Exemple :

10000 × 15 / 100 = 1500
🔍 Explication des principaux composants
MainActivity

Point d'entrée de l'application.

Elle initialise :

setContent {
    TipCalculatorTheme {
        TipTimeLayout()
    }
}

et affiche l'interface utilisateur.

TipTimeLayout()

Fonction principale de l'interface.

Elle contient :

les champs de saisie ;
le bouton d'arrondi ;
l'affichage du résultat.

Elle utilise :

remember { mutableStateOf() }

pour gérer les données saisies par l'utilisateur.

EditNumberField()

Composant réutilisable permettant de créer un champ de saisie.

Il reçoit :

un label ;
une icône ;
un type de clavier ;
une valeur.

Exemple :

EditNumberField(
    label = R.string.bill_amount
)
RoundTheTipRow()

Cette fonction affiche le bouton permettant d'activer ou désactiver l'arrondi.

Elle utilise :

Switch()
📦 Installation
Prérequis

Avant d'exécuter le projet, il faut avoir :

Android Studio installé
JDK installé
Un émulateur Android ou un téléphone connecté
Étapes
Cloner le projet :
git clone https://github.com/votre-compte/TipCalculator.git
Ouvrir le projet dans Android Studio.
Synchroniser Gradle.
Lancer l'application avec :
Run ▶
🎨 Interface utilisateur

L'application utilise :

Column pour organiser les éléments verticalement ;
Row pour la ligne d'arrondi ;
TextField pour les entrées ;
Text pour afficher les résultats ;
Switch pour l'option d'arrondi.
🔮 Améliorations possibles

Quelques améliorations futures :

Ajouter plusieurs devises (FCFA, €, $, etc.)
Ajouter un historique des calculs
Ajouter un thème sombre
Ajouter une animation lors du calcul
Ajouter un bouton de partage du résultat
