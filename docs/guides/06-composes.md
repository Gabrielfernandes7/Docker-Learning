# Docker Compose 🚀

Docker Compose é a ferramenta para definir e gerenciar aplicações Docker multi-contêiner.

## Estrutura Básica do `docker-compose.yml` 📄

```yaml
version: '3'
services:
  web:
    image: nginx
    ports:
      - "80:80"
  db:
    image: mysql
    environment:
      MYSQL_ROOT_PASSWORD: example
```

### Principais Diretrizes 📌

- **`services`**: Cada serviço é um contêiner que faz parte da aplicação.

- **`image`**: Define a imagem que será utilizada no serviço. Especifica o que o contêiner precisa para funcionar.

- **`build`**: Define o processo de construção de imagem a partir de um Dockerfile.

  ```yaml
  services:
    web:
      build:
        context: .
        dockerfile: Dockerfile
  ```

- **`ports`**: Define o mapeamento de portas entre o contêiner e o host. Necessário para expor serviços internos do contêiner ao mundo externo.

- **`volumes`**: Define volumes para persistir dados e compartilhar arquivos entre contêiner e o host. Fundamental para manter a persistência dos dados além do ciclo de vida do contêiner.

- **`environment`**: Define as variáveis de ambiente para os serviços. Permite configurar dinamicamente os serviços sem modificar a imagem.

- **`networks`**: Cria automaticamente uma rede para os serviços se comunicarem. Redes podem ser definidas manualmente para maior controle.

  ```yaml
  services:
    web:
      image: nginx
      networks:
        - frontend
    db:
      image: mysql
      networks:
        - backend

  networks:
    frontend:
    backend:
  ```

- **`depends_on`**: Define a ordem de inicialização dos serviços.

  ```yaml
  services:
    web:
      image: nginx
      depends_on:
        - db
  ```

## Comandos Úteis 🛠️

- **Executar e iniciar todos os serviços definidos no `docker-compose.yml`**:

  ```sh
  docker-compose up
  ```

- **Reconstruir as imagens antes de iniciar os contêineres**:

  ```sh
  docker-compose up --build
  ```

- **Escalar serviços facilmente**:

  ```sh
  docker-compose up --scale web=3
  ```

- **Criar um volume**:

  ```sh
  docker volume create app-dados
  ```

- **Inspecionar um volume**:

  ```sh
  docker volume inspect app-dados
  ```

- **Executar um contêiner com um volume montado**:

  ```sh
  docker run -d -p 3000:3000 --name kiwi -v app-dados:/app app-image
  ```

### Conclusão 📚

Esses conceitos e comandos cobrem a maior parte das necessidades comuns ao usar Docker Compose, permitindo criar, gerenciar e escalar aplicações multi-contêiner de maneira eficiente e escalável.