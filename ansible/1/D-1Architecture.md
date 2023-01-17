# Architecture

- Nous utilisation Vagrant pour deployer notre Server/VM.
- Nous utilisation Ansible pour la configuration des resources.
- URL mise en place : [numeration](http://wwww.numeration.com)

### Structure des fichiers :
```schell
D-DevSecOps-B3-GDPROG-eval-pratique
├── LICENSE
├── README.md
├── ansible
│   ├── 1
│   │   └── D-1Architecture.md
│   ├── 2
│   │   └── user_and_group.yml
│   ├── 3
│   │   ├── dependences_bdd.yml
│   │   └── dependences_wordpress.yml
│   ├── 4
│   │   ├── automatisation_wordpress_bdd.yml
│   │   ├── automatisation_wordpress_deploiment.yml
│   │   └── wordpress
│   │       ├── bd_numeration.sql
│   │       └── numeration.tar.gz
│   ├── 5
│   │   ├── serveur_bdd
│   │   │   └── firewall_rules.yml
│   │   ├── serveur_web
│   │   │   └── firewall_rules.yml
│   │   └── ufw_install.yml
│   ├── 7
│   │   └── pam_pwquality.yml
│   ├── site.yml
│   └── var_file.yml
└── vagrant
    ├── Vagrantfile
    └── ssh_keys
        ├── devsecops
        └── devsecops.pub

13 directories, 19 files

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
