# Elixir Docker - (Linux)

```bash
docker build -t meu_elixir .
```

```bash
docker run --rm -v $(pwd):/app/meu_projeto meu_elixir elixir hello.exs
```
