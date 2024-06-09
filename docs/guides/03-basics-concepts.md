# Conceitos básicos do Docker

### 1. Dockerfile

É um arquivo de texto que possui passo a passo para construir uma imagem Docker.

Pense no Dockerfile como um a receita de bolo e nossa imagem docker sendo o bolo.

<p align="center">
    <img height="270px" width="270px"
        src="/docs/images/cooking-image-docker.jpeg"
        alt="Whale Cooking"
    />
</p>

`FROM`: qual imagem meu dockerfile irá carregar

`WORKDIR`: diretório de trabalho, serve para especificar me que pasta se encontra nossa aplicação.

`COPY` e `ADD`: esses dois comandos servem para copiar e criar/adicionar todos os arquivos que fazem parte da minha aplicação dentro da minha imagem.

`RUN`: execute a aplicação, execute este processo.

`ENV`: enviroment, nossas variáveis de ambiente, por exemplo, quando quero colocar a url de uma api.

```dockerfile
ENV API_URL=http://localhost:8080/
```

`EXPOSE`: serve para informar quais portas os containeres irá utilizar para executar as requisições

`CMD`: define o comando padrão a ser executado quando o container é iniciado

`ENTRYPOINT`: é para configurar o ambiente do container

```shell
# abrir nossa imagem no terminal
docker run -it <nome-da-imagem-que-criamos> sh
```

### 2. Imagem Docker

Uma imagem é um pacote estático que inclue sua aplicação com todos seus componente (bibliotecas, códigos, configurações, etc.) necessários para executar. As imagens são usadas para criar contêineres.

### 3. docker-compose.yml

É um arquivo de configuração utilizado para configurar e executar vários
serviços como os meus contâineres.

Objetivo: Orquestração(Gerenciamento) de vários containêres.

### Referências

[Dockerfile instruções](https://docs.docker.com/reference/dockerfile/)