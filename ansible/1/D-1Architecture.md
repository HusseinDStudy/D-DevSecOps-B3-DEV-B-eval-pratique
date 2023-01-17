# Architecture

- Nous utilisation Vagrant pour deployer notre Server/VM.
- Nous utilisation Ansible pour la configuration des resources.
- URL mise en place : [numeration](http://wwww.numeration.com)

## Configuration du fichier host
Accéder au fichier hosts de votre system 
```shell
nano /etc/hosts
```
> Ajouter à la fin de votre fichier :
> 192.168.56.32      numeration.com

### Structure des fichiers :
```schell
D-DevSecOps-B3-GDPROG-eval-pratique/
├── ansible/
│   ├── /1
│   │   └──D-1Architecture.md
│   ├── /2
│   │   └── user_and_group.ymal
│   ├── /3
│   │   ├── wordpress/
│   │   │   ├── bd_numeration.sql
│   │   │   └── numeration.tar.gz
│   │   └── dependences_wordpress.yml
│   ├── /5
│   │   ├── 
│   │   └──
│   ├── /6
│   │   ├── 
│   │   └──
│   ├── /7
│   │   └──
│   └── /site.yml
├── vagrant/
│   ├── /.vagrant
│   └── Vagrantfile
├── LICENSE
└── README.md
```

### Vagrant configuration

| Serveur VM #1                              | Interconnection                                   | Serveur VM #2                                    |
|--------------------------------------------|---------------------------------------------------|--------------------------------------------------|
| <div style="margin: auto;">WEB(HTTP)</div> | <span style="color:#eab676" ><===========></span> | <div style="width: 50%; margin: auto;">BDD</div> |

### Command execution sur le bureau
```Shell
cd ~desktop/vagrant
vagrant up
vagrant ssh
```
