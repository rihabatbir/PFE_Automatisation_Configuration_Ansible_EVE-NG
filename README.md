# PFE_Automatisation_Configuration_Ansible_EVE-NG
Projet de fin d'études sur l'automatisation des configurations réseau avec Ansible et l'environnement de virtualisation EVE-NG
#### Préparation 

Réunion de démarrage du projet
Définition des objectifs 
Conception de l'architecture de l'automatisation de configuration
Création de schémas de flux de travail et de diagrammes de processus
definition d'architecture d'ansible
Etude de la solution


#### Phase de Développement initial
Installation et configuration de VMware Workspace
Installation et configuration de Ubuntu et kali 
Installation d'Ansible dans Ubuntu 
Installation d'EVN-EG dans VMware
installation de winscp
installation putty
Installation des images iso switch routeur .. et fixer les permissions

#### Développement de la fonctionnalité principale
##### Création d'un laboratoire

Le laboratoire se compose de trois switches et les mahines(VPCS).
Un switch est configuré en tant que serveur VTP et VLAN 1.
Deux switches sont configurés en tant que clients VTP.
Nous avons configuré SSH sur les switches.
Nous avons testé le ping et SSH sur le laboratoire .

##### Implémentation de l'automatisation de la configuration

Nous avons configuré un fichier ansible.cfg pour une configuration cohérente, sécurisée et optimisée des opérations automatisées avec Ansible.
Nous avons utilisé les fichiers d'inventaire inventory.ini et hosts pour organiser, centraliser et gérer les informations des hôtes de manière efficace.

##### Écriture du code pour automatiser les processus de configuration
Nous avons utilisé les playbooks Ansible, qui sont des fichiers écrits en YAML définissant une série de tâches d'automatisation à exécuter sur des hôtes.
Un playbook pour obtenir des informations sur les switches.
Un playbook pour tester le ping sur les switches.
Un playbook pour configurer les VLANs sur les switches.
##### Tests unitaires et intégration continue pour assurer la fiabilité
Nous avons testé la création des VLANs sur les switches.
Nous avons testé le ping entre les machines.

#### Utilisation de l'outil de gestion de versions et des configurations dans le développement logiciel  : Git 

Git joue un rôle essentiel dans l'utilisation d'Ansible, en fournissant une base solide pour la gestion des configurations et la collaboration sur les playbooks. Voici comment Git est intégré dans les workflows Ansible 

1. Gestion de la Configuration
Git permet de suivre toutes les modifications apportées aux playbooks Ansible. Chaque changement est enregistré sous forme de commit, ce qui facilite la gestion des différentes versions et le retour à une version antérieure si nécessaire.

2. Collaboration
Git permet à plusieurs utilisateurs de travailler sur les mêmes fichiers de manière simultanée. Les développeurs peuvent cloner le dépôt Git, apporter leurs modifications et soumettre des pull requests pour révision.
3. Intégration Continue (CI) et Déploiement Continu (CD)
Tests Automatisés : En intégrant Git avec des outils de CI/CD (comme GitHub Actions), nous avons automatiser les tests de vos playbooks Ansible. Chaque fois qu'un changement est poussé dans le dépôt, les tests sont exécutés pour s'assurer que les nouvelles configurations ne cassent rien.
