# D-DevSecOps-B3-GDPROG-eval-pratique

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
> <span style="color:red"> Il fait modifier les mots de passe dans le var_file.yml afin de Sécurisé son system !</span>

```shell
# déplacer le fichier de clé ssh dans votre dossier publique
mv vagrant/ssh_keys/* ~/.ssh/

# On déplace le terminal dans le rep vagrant
cd vagrant/

# Puis on execute le vagrant fille
vagrant up

# la machine est presque prêt 😁
```
### Configuration du fichier host
> Cette étape permet d'accéder au site via votre navigateur sur l'url http://numeration.com

#### Accéder au fichier hosts de votre system :
```shell
sudo nano /etc/hosts
# Ajouter cette ligne dans votre fichier hosts
192.168.56.32   www.numeration.com numeration.com
```

## Teste le deployment
Il est de suivre ce lien [Numeration](http://numeration.com) sur votre navigateur



### Information Provider
> Cette version fonctionne également sur Parallels, avec une puce de mac M1

Commenter la partie non désire dans le fichier vagrant fille

### Rappel de command vagrant : 
><span style=color:green>Les commands sont à exécuter dans le rep vagrant</span>

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
