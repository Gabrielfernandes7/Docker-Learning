# Mapeamento de portas (redirecionamento de portas)

O mapeamento de portas no Docker é um recurso crucial para permitir que você tenha
acesso a serviços executados dentro de containers Docker a partir da sua máquina
local.

```shell
docker run -d -p <host>:<docker>
```

```shell
docker run -d -p host:docker --name nome_container imagem base
```

Todo tráfego que ocorrer na portal `host` é redirecionado para a porta do container `docker`, no exemplo acima.

