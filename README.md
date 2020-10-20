# curso_ansible_tower

## tareas para instalacion

Ansible <-----

Ansible Towe AWX <------

sudo apt update
sudo apt install software-properties-common
sudo apt-add-repository --yes --update ppa:ansible/ansible
sudo apt install ansible --yes

###  Ansible Tower AWX
    Docker            sudo apt install docker
    Docker-compose    sudo apt install docker-compose
                      sudo pip install docker-py
    NodeJs  (interprete de javascript)
                      sudo apt install nodejs
    NPM Gestor de paquetes para java script  (como el pip de python, pero para java)
                      sudo apt install npm
    configurar npm en la maquina  (para que sea ejecutable desde cualquier sitio)
                      sudo npm install npm --global
    mirar la pagina  github.com/ansible/awx   y mirar la instal guide
    
    instalacion de ansible tower awx: 
    
    Modificamos el fichero inventory, y ponemos otro puerto:  host_port=8080  porque el puerto 80 aws se lo asigno a otra cosa
    Ademas debemos crear una clave cruzada con el pwgen  y ponerla en el inventory
    en el campo:    secret_key=xxxxxxxxxxxxxxxxx   (la key que se genero  con el pwgen)
    
    Si se tiene todos los prerequisitos, instalamos ansible tower como un playbook: 
        Hay problemas si no es root en la maquina, asi que nos hacemos root:   sudo su -
        cd /root/awx/installer
        ansible-playbook -i inventory install.yml
        
        
                      


