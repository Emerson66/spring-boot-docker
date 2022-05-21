# Spring Boot com Docker

Este projeto tem o objetivo de servir como um guia para o processo de contrução de uma imagem Docker para rodar num projeto Spring Boot.

## O que você precisa para rodar este projeto

- Java 17
- Docker



## Ubuntu

### Pré-requisitos
- Ubuntu acima de 18.04 (LTS).
- arquiteturas: x86_64 (ou amd64), armhf, arm64, e s390x.

### Instalando Docker

```` sh
sudo apt-get remove docker docker-engine docker.io containerd runc
sudo apt-get update 
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
    
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
  
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
sudo docker run hello-world
````

#### Instalando Java 17

``` sh
sudo apt install openjdk-17-jdk-headles
```
