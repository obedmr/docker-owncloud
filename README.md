# docker_owncloud
OwnCloud Docker container with SSH access


1. Pull docker image

  ```docker pull obedmr/owncloud```
  
2. Start your container

  ``` docker run -d -v /srv/data/html:/var/www/html -p 80:80 -p 2222:22 -e ROOT_PASS="mypass" obedmr/owncloud ```
  
  - Note:
    - ```/srv/data/html``` is the host's directory that you will share with the container
    - ```-p 80:80``` You're forwarding the 80 container port to the host's 80 port
    - ```-p 2222:22``` You're forwarding the 22 container port to the host's 2222 port
    - ```ROOT_PASS``` specifies the root password you want for the container's root user
    
3. And ... that's all
  - You can access the OwnCloud web interface at http://localhost/
  - You can login by ssh to your container by running:
  
    ``` ssh root@localhost -p 2222 ```
  
4. Enjoy and feel free to contribute

@obedmr
obed.n.munoz@gmail.com
