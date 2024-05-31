# Aprendendo Docker 
<p align="center">
    <img height="150px" width="150px"
        src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original-wordmark.svg"
        alt="Docker"
    />
</p>

## Índice
1. [Introdução](/docs/guides/01-introduction.md)
2. [Instalação](/docs/guides/02-get-docker.md)
3. [Conceitos Básicos](#conceitos-básicos)
   - [Container e Containerização](#1-container-e-containerização)
   - [Imagem Docker](#2-imagem-docker)
   - [Dockerfile](#3-dockerfile)
   - [Docker-compose.yml](#4-docker-composeyml)
4. [Exemplos](/exemples/exemples.md)
5. [Recursos Adicionais](#recursos-adicionais)
6. [Licença](#licença)

## Soluções que o Docker traz (A mágica do Docker)

<p align="center">
    <img height="270px" width="270px"
        src="./docs/images/docker-magician.jpeg"
        alt="Whale magician"
    />
</p>

Facilita o deploy no ambiente de produção. Pois consigo montar o ambiente virtual de minha aplicação e rodar no servidor.

## Conceitos básicos do Docker

### 1. Container e containerização

Um container é uma instância em execução de uma imagem Docker.

Os containeres permitem empacotar a aplicação e suas dependências
em um ambiente isolado. Garantindo a consistência na execução
da aplicação em diferentes ambientes.

### 2. Imagem Docker

Uma imagem é um pacote estático que inclue sua aplicação com todos seus componente (bibliotecas, códigos, configurações, etc.) necessários para executar. As imagens são usadas para criar contêineres.

### 3. dockerfile

É um arquivo de texto que possui passo a passo para construir uma imagem Docker. Descreve os comando necessários para montar e configurar o container.

### 4. docker-compose.yml

É um arquivo de configuração utilizado para configurar e executar vários
serviços como os meus contâineres.

Objetivo: Orquestração(Gerenciamento) de vários containêres.
