# D-DevSecOps-B3-GDPROG--val-pratique
# Provider
> Cette version fonctionne également sur Parallels, avec une puce de mac M1
```shell
git checkout name/function
git add /path/to/file/to/add
git commit -a -m "message" - m "descreption"
git push
cp vagrant/ssh_keys/* ~/.ssh
``` 
# Information de configuration
## Configuration du fichier host
Accéder au fichier hosts de votre system :
```shell
nano /etc/hosts
```
> Ajouter à la fin de votre fichier :
> 192.168.56.32      numeration.com

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
