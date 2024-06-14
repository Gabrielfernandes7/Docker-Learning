# Comandos úteis do Docker

```shell
# listar todos containeres em execução
docker container ps -a
```

```shell
# listar todas imagens em execução
docker images -a
```

**Como apagar volumes, containeres e Images**

[How To Remove Docker Images, Containers, and Volumes](https://www.digitalocean.com/community/tutorials/how-to-remove-docker-images-containers-and-volumes#remove-dangling-docker-images)

```shell
# remove os containers parados e as imagens não utilizadas
docker system prune -a
```

**Imagem do Linux rodando em um container**

```shell
docker run -it ubuntu
```

Dentro do mesmo terminal, estaremos executando comandos do Linux.

```shell
whoami # comando para saber o nome do usuário do meu OS
```

```shell
echo $0 # saber a pasta e o diretório
```

**Saber os arquivos que estão dentro da minha imagem**

```shell
docker exec nome_container ls
```
