# D-DevSecOps-B3-DEV-B-eval-pratique

### Configuration du projet
- Virtual-Box (Version 6.1.x max) ou Parallels (18.1.1)(Mac M1)
  
- Plugins provider :
    - vagrant-vbguest (Virtual-Box)
    - vagrant-parallels (Parallels)

- 16 GB de RAM (recommender)
- Vagrant (2.3.3)
- Ansible (core 2.14.1)
- Python (3.11.1)

# Étape de configuration du wordPress :
> <span style="color:red"> Placer vous dans le répertoire du projet !</span>
### Securité :
> <span style="color:red"> Il faut modifier les mots de passe dans le var_file.yml afin de sécuriser son système !</span>

```shell
# déplacer le fichier de clé ssh dans votre dossier publique
mv vagrant/ssh_keys/* ~/.ssh/

# On déplace le terminal dans le répertoire vagrant
cd vagrant/

# Puis on execute le vagrant file
vagrant up

# La machine est presque prête 😁
```
### Configuration du fichier host
> Cette étape permet d'accéder au site via votre navigateur sur l'url http://numeration.com

#### Accéder au fichier hosts de votre system :
```shell
sudo nano /etc/hosts
# Ajoutez cette ligne dans votre fichier hosts
192.168.56.32   www.numeration.com numeration.com
```

## Teste le deployment
Il vous suffit de suivre ce lien [Numeration](http://numeration.com) sur votre navigateur



### Information Provider
> Cette version fonctionne également sur Parallels, avec une puce de mac M1

Commentez la partie non désirée dans le fichier vagrant file

### Rappel de commande vagrant : 
><span style=color:green>Les commandes sont à exécuter dans le répertoire vagrant</span>

````shell
# Démarre les vm ou lance la creation et leur provision
vagrant up
# Information sur le status de la vm
vagrant status 
# Connection a la machine en SSH
vagrant ssh
# Apple la provision des vm (appel du playbook)
vagrant provision 
# Détruite les machine virtuel
vagrant destroy 
# Liste les machine connue de vagrant
vagrant global-status 
# supprimer les information invalide de la liste des machine de vagrant
vagrant vagrant global-status --prune
# Dans le doute il est recommender dans ce contexte de supprimer également le .vagrant
rm -r .vagrant
````
