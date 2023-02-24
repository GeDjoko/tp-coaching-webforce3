# tp-coaching-webforce3
Instruction pour la session de coaching

##############################################################################################

## Exercice 1  - Scrum 
**Préparer le dashboard Scrum pour ce projet.**

création d'un project dans github
Faire une copie d'écran de votre dashboard et placez le fichier de l'image 
dans git/github pour qu'il soit versionné 

##############################################################################################

## Exercice 2  - Linux 
# Mise à jour des packages de la VM ubuntu  
sudo apt update && sudo apt upgrade -y

# Vérification de version de python3 déjà installée 
$ python3 -V

Le programme python est executé avec le nom python3, de votre VM 
sudo nano .bashrc

# creating another alias for python3
alias python='python3' 
# Fermer et reouvrir le terminal pour reactiver l'opération. Ou bien entr la commande:
$ source .bashrc 

# Verifier la l'alias avec:
ubuntu@coaching-4:~$ python -V
Python 3.8.10



vérifier en faisant  ```python -V```


Faire un ```pip install flask``` , suivre les instructions pour installer pip si nécessaire
sudo apt install python3-pip
sudo pip3 install flask
sudo pip3 install requests

##############################################################################################

## Exercice 3  - Storage 

Recherche le disque supplémentaire de 1Gb connecté à la VM, précisez la commande utilisée
Identifier la partition avec la commande 
fdisk -l
Disk /dev/vdc: 1 GiB, 1073741824 bytes, 2097152 sectors
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes

#Commande sudo lshw -class disk
  *-virtio3
       description: Virtual I/O device
       physical id: 0
       bus info: virtio@3
       logical name: /dev/vdc
       size: 1GiB (1073MB)
       configuration: driver=virtio_blk logicalsectorsize=512 sectorsize=512

Formattez ce disque au format ext4  

Formater la partition avec mkfs
sudo mkfs -t ext4 /dev/vdc
ubuntu@coaching-4:/home/tp-coaching-webforce3$ sudo mkfs -t ext4 /dev/vdc


Monter (mount) ce disque sur le point montage /home/ubuntu/tp-coaching-webforce3/log

sudo lshw -class disk

##############################################################################################
## Exercice 4  - Git/Github 

##############################################################################################

## Exercice 5  - Python

##############################################################################################

## Exercice 6  - Pare-feu 
