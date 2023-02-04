# Architecture

- Nous utilisation Vagrant pour deployer notre Server/VM.
- Nous utilisation Ansible pour la configuration des resources.
- URL mise en place : [numeration](http://wwww.numeration.com)

### Structure des fichiers :
```schell
D-DevSecOps-B3-GDPROG-eval-pratique
├── ansible
│   ├── 1
│   │   └── D-1Architecture.md
│   ├── 2
│   │   ├── enable_sudo.yml
│   │   ├── folder_for_website_deployment.yml
│   │   ├── ssh_keys.yml
│   │   └── user_and_group.yml
│   ├── 3
│   │   ├── dependences_db.yml
│   │   └── dependences_wordpress.yml
│   ├── 4
│   │   ├── automatisation_wordpress_db.yml
│   │   ├── automatisation_wordpress_deploiment.yml
│   │   └── wordpress
│   │       ├── apache.conf.j2
│   │       ├── bd_numeration.sql
│   │       └── numeration.tar.gz
│   ├── 5
│   │   ├── serveur_db
│   │   │   └── firewall_rules.yml
│   │   ├── serveur_web
│   │   │   └── firewall_rules.yml
│   │   └── ufw_install.yml
│   ├── site.yml
│   └── var_file.yml
├── LICENSE
├── README.md
├── Retex.md
└── vagrant
    ├── ssh_keys
    │   ├── devsecops
    │   └── devsecops.pub
    └── Vagrantfile

11 directories, 23 files


```

### Vagrant configuration

| Serveur VM #1                              | Interconnection                                   | Serveur VM #2                                    |
|--------------------------------------------|---------------------------------------------------|--------------------------------------------------|
| <div style="margin: auto;">WEB(HTTP)</div> | <span style="color:#eab676" ><===========></span> | <div style="width: 50%; margin: auto;">BDD</div> |