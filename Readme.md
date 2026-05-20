
 
# Practica 05 Ansible
## 1. Explica que es Ansible
Explica que es Ansible, y dentro del contexto de Ansible explica como se relacionan los siguientes terminos:


## 1.1. Inventario


## 1.2. Playbook


## 2. ¿Que es un ad-hoc command?



## Instalacion 

Ansible no se puede instalar de forma nativa en Windows. Para utilizarlo como "nodo de control" desde tu equipo, debes instalar el Subsistema de Windows para Linux (WSL) y ejecutarlo sobre una distribución de Linux (como Ubuntu), lo que te permitirá gestionar tus servidores desde la comodidad de tu entorno
``` shell 
wsl --install
```

``` bash 
sudo apt update && sudo apt upgrade -y

sudo apt install software-properties-common -y

sudo add-apt-repository --yes --update ppa:ansible/ansible

sudo apt install ansible -y
```
## 3. Crea un inventario con las siguientes características:


El nodo de control se encuentra en la IP: 192.168.56.10
Los nodos con arquitectura ARM en las IPs: 192.168.56.11, 192.168.56.12
Un nodo de arquitectura AMD en la IP: 192.168.56.13

rem creas el fichero
touch .my_inventory.ini 

```ini
[control]
192.168.56.10

[arm]
192.168.56.11
192.168.56.12
```


## 3.1 Crea grupos en el inventario por arquitectura de máquina, crea un grupo para el nodo de control

## 3.2 Crea un alias para el nodo de control

## 4. Explica el `built-in` module `ping`

```
ansible all -i ./my_inventory.ini -m ping 
```

## 5. Crea un Playbook que instale Docker