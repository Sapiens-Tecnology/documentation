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
