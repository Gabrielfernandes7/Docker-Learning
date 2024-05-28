# Use a imagem oficial do Elixir
FROM elixir:latest

# Instale o Hex, o gerenciador de pacotes do Elixir, e Rebar, uma ferramenta para construir projetos Erlang
RUN mix local.hex --force && mix local.rebar --force

# Defina o diretório de trabalho
WORKDIR /app

# Crie um novo projeto Elixir (substitua "meu_projeto" pelo nome do seu projeto)
RUN mix new meu_projeto

# Navegue para o diretório do projeto
WORKDIR /app/meu_projeto

# Copie os arquivos do projeto para o diretório de trabalho
COPY . .

# Instale as dependências do projeto
RUN mix deps.get

# Comando padrão para iniciar um shell do Elixir
CMD ["iex", "-S", "mix"]
