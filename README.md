# pyvmomi_ESXi_VM_Manager
Automatisation et simplifica# PyVmomi ESXi VM Manager

**PyVmomi ESXi VM Manager** est un outil de gestion de machines virtuelles pour VMware ESXi, conçu pour automatiser les processus de déploiement, de clonage et de création de machines virtuelles (VM) via des scripts Python et la bibliothèque `pyvmomi`.

## Table des matières

- [Installation](#installation)
- [Configuration](#configuration)
- [Utilisation](#utilisation)
- [Scripts Disponibles](#scripts-disponibles)
- [Dépendances](#dépendances)
  
## Installation

1. Clonez ce dépôt :
   ```bash
   git clone (https://github.com/princiliz/pyvmomi_ESXi_VM_Manager)
   cd pyvmomi_ESXi_VM_Manager

2. Installez les dépendances requises :
   ```bash
   pip install -r requirements.txt
   ```

## Configuration

Les configurations pour les différents scripts sont définies dans le répertoire `configs`. Voici un aperçu de chaque fichier de configuration :

- **configDeployVM.json** : Configure les paramètres de déploiement d'une VM depuis une image OVA.
- **configCloneVM.json** : Définition des options pour le clonage d'une VM existante.
- **configCreateVM.json** : Configuration pour la création d'une VM avec des paramètres personnalisés.

Assurez-vous de modifier ces fichiers JSON en fonction de votre environnement et de vos besoins spécifiques.

## Utilisation

Chaque script dans le dossier `scripts` est conçu pour exécuter une opération spécifique sur les VM. Par exemple :

- Pour déployer une VM à partir d'une image OVA :
  ```bash
  python scripts/deploy_OVA_VM.py
  ```
- Pour cloner une VM :
  ```bash
  python scripts/clone_OVA_VM.py
  ```
- Pour créer une nouvelle VM avec des configurations spécifiques :
  ```bash
  python scripts/create_VM.py
  ```

## Scripts Disponibles

### deploy_OVA_VM.py
Déploie une VM à partir d'un fichier OVA spécifié dans `configDeployVM.json`.

### clone_OVA_VM.py
Clone une VM existante avec les paramètres définis dans `configCloneVM.json`.

### create_VM.py
Crée une VM vierge avec les spécifications fournies dans `configCreateVM.json`.

### utils/vsphereConnection.py
Ce fichier utilitaire gère la connexion au serveur vSphere pour interagir avec l'API VMware.

## Dépendances

Les dépendances nécessaires pour exécuter ces scripts sont listées dans `requirements.txt`. Assurez-vous que `pyvmomi` est installé pour interagir avec l'API VMware ESXi :

```text
pyvmomi>=7.0.3

```

Ce README est prêt pour une utilisation dans ton fichier `README.md` !
