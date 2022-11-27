## Jenkins server need to install Docker because Jenkin need to push image to docker registry 
## Install Docker 
```sh
yum install docker
systemctl start docker
systemctl enable docker
```

## Provide permissions to "jenkins" user in Jenkins server to access and use Docker
```sh
  sudo groupadd docker
  sudo usermod -aG docker jenkins
  sudo chmod 777 /var/run/docker.sock
```
## Add Jenkins user into sudoers file to get sudo access
```sh
   vi /etc/sudoers
   jenkins ALL=(ALL) NOPASSWD: ALL
```   
   

