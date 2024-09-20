---
title: Installation de l'ERP en local sur un poste Windows
---




## 1. Installation de SQL Server Express

**SQL Server Express** : ![[SQLEXPR_x64_FRA.exe]]
### Étape 1 : Installation de **SQL Server Express**
1. Exécuter le fichier **SQLEXPR_x64_FRA.exe**.
2. Sélectionner **Nouvelle installation**.
3. Accepter les termes du contrat de licence.
4. Laisser les options par défaut jusqu'à l'étape de configuration du serveur.

### Étape 2 : Configuration du moteur de base de données
1. À l'étape de **Configuration du moteur de base de données**, choisir **Mode mixte**.
2. Définir un mot de passe facile à retenir pour l'utilisateur **SA**.
3. Cliquer sur **Suivant**.

### Étape 3 : Options supplémentaires
1. Ne pas cocher l'option d'envoi des données à Microsoft.
2. Cliquer sur **Suivant**, puis **Fermer** une fois l'installation terminée.

---

## 2. Installation de SQL Server Management Studio (SSMS)

**SQL Server Management Studio :** ![[SSMS-Setup-FRA.exe]]
### Étape 1 :Installation de **SQL Server Management Studio**
1. Exécuter le fichier **SSMS-Setup-FRA.exe**.
2. Laisser l'emplacement par défaut.
3. Cliquer sur **Installer**.
4. Fermer l'installateur une fois l'installation terminée.

---

## 3. Installation de Visual Studio Code

**Visual Studio Code :** ![[VSCodeUserSetup-x64-1.79.2.exe]]
1. Télécharger et installer **Visual Studio Code** depuis le site officiel.
2. Suivre les étapes d'installation par défaut.

---

## 4. Installation des composants ODBC et SQL

**ODBC :** ![[msodbcsql 1.msi]]
### Étape 1 : Installation de **msodbcsql.msi**
1. Exécuter **msodbcsql.msi** et suivre les étapes d'installation.

**SQL :** ![[sqlncli (1).msi]]
### Étape 2 : Installation de **sqlncli.msi**
1. Exécuter **sqlncli.msi** et suivre les étapes d'installation.

---

## 5. Installation de XAMPP

**XAMPP :**  ![[xampp-win32-1.7.5-VC9-installer 1.exe]]
### Étape 1 : Installation de **XAMPP**
1. Exécuter l'installateur de XAMPP.
2. Lors de l'installation, cocher les options suivantes :
   - **Apache as a service**
   - **SQL as a service**
   
### Étape 2 : Configuration de PHP pour SQL Server
1. Accéder au répertoire d'installation de XAMPP, puis naviguer vers le dossier **php**, ensuite vers **ext**.
2. Copier les fichiers suivants dans le dossier **ext** :
   - **php_pdo_sqlsrv_53_ts.dll :** ![[php_pdo_sqlsrv_53_ts.dll]]
   - **php_sqlsrv_53_ts.dll** : ![[php_sqlsrv_53_ts.dll]]


### Étape 3 : Modification du fichier **php.ini**
1. Revenir dans le dossier **php** et ouvrir le fichier **php.ini**.
2. Rechercher la section des **extensions Windows**.
3. Ajouter les lignes suivantes à la suite des extensions existantes :
   extension=php_pdo_sqlsrv_53_ts.dll
   extension=php_sqlsrv_53_ts.dll
4. Enregistrer les modifications et fermer le fichier.

## 6. Finalisation

1. Redémarrer votre ordinateur pour appliquer toutes les modifications.


---

## 7. Installation de GitHub Desktop

### Étape 1 : Téléchargement de **GitHub Desktop**
1. Rendez-vous sur le site officiel de GitHub Desktop : [desktop.github.com](https://desktop.github.com).
2. Cliquez sur le bouton **Download for Windows** (ou pour votre système d'exploitation).

### Étape 2 : Installation de **GitHub Desktop**
1. Ouvrez le fichier téléchargé (ex. **GitHubDesktopSetup.exe**).
2. Suivez les instructions à l'écran pour installer l'application.
3. Une fois l'installation terminée, lancez **GitHub Desktop**.

### Étape 3 : Connexion à GitHub
1. À la première ouverture de l'application, cliquez sur **Sign in to GitHub.com**.
2. Entrez vos identifiants GitHub (ou créez un compte si vous n'en avez pas).
3. Autorisez l'application à accéder à votre compte GitHub.

### Étape 4 : Configuration de Git
1. Dans GitHub Desktop, allez dans **Fichier** > **Options** (ou **Preferences** sur macOS).
2. Dans l'onglet **Git**, vérifiez que vos informations de nom d'utilisateur et adresse e-mail sont correctement renseignées (elles seront utilisées pour vos commits Git).

### Étape 5 : Clonage ou création de dépôts
1. Pour cloner un dépôt GitHub existant, cliquez sur **File** > **Clone repository**, et suivez les instructions.
2. Pour créer un nouveau dépôt, cliquez sur **File** > **New repository** et configurez-le selon vos besoins.

