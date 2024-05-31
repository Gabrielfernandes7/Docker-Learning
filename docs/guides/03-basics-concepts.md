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

### 2. Imagem Docker

Uma imagem é um pacote estático que inclue sua aplicação com todos seus componente (bibliotecas, códigos, configurações, etc.) necessários para executar. As imagens são usadas para criar contêineres.

### 3. docker-compose.yml

É um arquivo de configuração utilizado para configurar e executar vários
serviços como os meus contâineres.

Objetivo: Orquestração(Gerenciamento) de vários containêres.