# Steps to setup


## What are we going to build?
```
Browser
|
v
NGINX (Port 80) ← Load Balancer
|
|-- App1 (Flask) :5000
|-- App2 (Flask) :5000
|-- App3 (Flask) :5000
```

# install and setup docker & docker-compose

``` bash
sudo apt update -y
sudo apt install -y docker.io docker-compose
sudo systemctl enable docker
sudo systemctl start docker
sudo usermod -aG docker $USER
newgrp docker
docker --version
docker-compose --version
```

# Project-Strcuture:
```
nginx-docker-lb/
├── docker-compose.yml
├── nginx/
│   └── nginx.conf
└── app/
    ├── Dockerfile
    └── app.py
```

Create a folders and files as same as above structure and update the code and script by navigating to the folder in the current directory. or pull the github code and follw the below commands.

``` bash

cd nginx-docker-lb
docker-compose up -d --build
docker ps
```

and now try to access your app ny hitting publicIP of instance with port 80

# Example:
```
  http://<SERVER-IP>:80
```


