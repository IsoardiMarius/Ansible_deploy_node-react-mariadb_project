# Introduction

#### Si vous n'êtes pas familier avec Ansible : Un tutoriel est mis à votre disposition, il vous permettra de comprendre les bases d'Ansible, vous serez guidé pas à pas pour déployer l'application sur votre machine virtuelle : [Tutoriel Ansible](https://picayune-promotion-42d.notion.site/Mac-M1-deployment-Ansible-with-Debian-11-node-mysql-react-c21dbb0acc2d443e97079077e5b733e2)

Ce repository contient les sources pour le déploiement avec Ansible d'une app react connecter à un backend nodejs, qui est lui même connecter à une base de donnée mariadb.
Cette config Ansible est assez basique et ne contient pas de rôles, ni de variables ect ...

#### Pour une approche plus complète, je vous invite à regarder le repo [ansible-galaxy-react-node](https://github.com/IsoardiMarius/ansible-galaxy-node-react)

Pour résumer, Ansible est un outil d'automatisation qui permet de simplifier la gestion des serveurs, des applications et des infrastructures informatiques. Il utilise des fichiers de configuration simples pour décrire les tâches à effectuer.  
Grâce à Ansible, vous pouvez automatiser des tâches répétitives, déployer des applications plus rapidement et maintenir votre infrastructure sous contrôle de manière plus efficace. C'est un outil puissant et facile à utiliser, idéal pour les débutants souhaitant automatiser leurs opérations informatiques.


## Requirements

- Une machine virtuelle avec un OS Debian 11
- Ansible sur votre machine en locale

## Installation
- Commencer par cloner le repo sur votre machine
- Copier les fichiers inventory et playbook.yml dans le dossier /etc/ansible
- Modifier le fichier inventory avec les informations de votre machine virtuelle
- Lancer la commande ansible-playbook -i inventory playbook.yml -vvv



```bash
# Clone the repo
git clone https://github.com/IsoardiMarius/ansible-node-react.git

# Move files
mv ansible-node-react/inventory /etc/ansible
mv ansible-node-react/playbook.yml /etc/ansible

# Modifier le fichier inventory avec les informations de votre machine virtuelle
nano /etc/ansible/inventory

# Run ansible
ansible-playbook -i inventory playbook.yml -vvv 
```



