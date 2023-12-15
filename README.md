# Aprendendo Docker 
<img height="90px" width="90px" 
    src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original-wordmark.svg"
    alt="Docker"
/>

## Instalação do `Docker` (Ubuntu)

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

```yml
# docker-compose.yml
version: '3.8'

services:
  # Serviço para o aplicativo Spring Boot
  spring-app:
    build: ./path/to/your/spring-app  # Caminho para o diretório do seu aplicativo
    ports:
      - "8080:8080"  # Porta do host: Porta do contêiner
    depends_on:
      - postgres-db  # Dependência do banco de dados PostgreSQL
    environment:
      SPRING_DATASOURCE_URL: jdbc:postgresql://postgres-db:5432/db_name  # URL do banco de dados
      SPRING_DATASOURCE_USERNAME: your_username  # Usuário do banco de dados
      SPRING_DATASOURCE_PASSWORD: your_password  # Senha do banco de dados

  # Serviço para o banco de dados PostgreSQL
  postgres-db:
    image: postgres:latest
    ports:
      - "5432:5432"  # Porta do host: Porta do contêiner
    environment:
      POSTGRES_DB: db_name  # Nome do banco de dados
      POSTGRES_USER: your_username  # Usuário do banco de dados
      POSTGRES_PASSWORD: your_password  # Senha do banco de dados
```

