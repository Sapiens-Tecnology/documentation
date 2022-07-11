# DevOps

## Docker

Instalação docker no Linux

```shell
  sudo apt-get update
  sudo apt-get install docker.io
  sudo systemctl start docker
  sudo systemctl enable docker
  curl -L "https://github.com/docker/compose/releases/download/{version}/docker-compose-$(uname -s)-$(uname -m)" > ./docker-compose
  sudo mv ./docker-compose /usr/bin/docker-compose
  sudo chmod +x /usr/bin/docker-compose
```

Limpeza de imagens órfans

```shell
  docker rmi $(docker images -f dangling=true -q)
```

Lista de IPs para os webservices

- Produção
  - message-service - 172.26.0.2:8086 - https://api.sapiensbank.com.br:8186
  - av-server - 172.26.0.3:8056 - https://api.sapiensbank.com.br:8156
  - webserver-stable - 172.26.0.4:80 - https://api.sapiensbank.com.br
  - webserver-tmp - 172.26.0.5:81 - https://api.sapiensbank.com.br:8080

- Sandbox
  - message-service - 172.28.0.2:8186
  - webserver-stable - 172.26.0.3:80
  - av-server - 172.28.0.4:8156