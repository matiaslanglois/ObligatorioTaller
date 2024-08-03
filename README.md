# Obligatorio Linux 2024

Conjunto de PlayBooks que nos permiten configurar la infraestructura necesaria para un servicio de aplicación Web en una distribución RedHat (CentOS 9) y un servicio de base de datos en una distribución Debian (Ubuntu 24.4)

## Instalación

Se instala Ansible usando pipx

```bash
$ sudo dnf install python3-pip
$ pip install pipx
$ pipx ensurepath
$ pipx install ansible-core
$ pip inject ansible-core argcomplete
$ pipx inject ansible-core argcomplete
$ pipx inject ansible-core lint
$ activate-global-python-argcomplete --user
$ . /home/sysadmin/.bash_completion
```

## Uso
Se instalan los requerimientos necesarios para el funcionamiento de los modulos utilizados.
Se ejecuta el PlayBook site.yml el cual corre el conjunto de PlayBooks de forma ordenanda. 

```bash
$ ansible-galaxy collection install -r collections/requirement.yml
$ ansible-playbook -i inventory/hosts playbooks/site.yml --ask-become-pass
```

## Creditos

Matias Langlois y Victor Mendez
