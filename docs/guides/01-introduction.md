# Introdução

## O que é Docker?

É uma plataforma que foi criada para você contruir, rodar e transferir aplicações do seu ambiente de teste ou desenvolvimento para o ambiente em produção

**VM x Container**:

***VM (Máquina Virtual)***

* É uma máquina virtual completa, com seu próprio sistema operacional, kernel e espaço de memória.

* Cada VM é uma máquina independente, com seu próprio sistema operacional e configuração.

* Requer um hipervisor (ou virtual machine monitor) para rodar.

* O processo de criação e configuração de uma VM é mais complexo e demorado.

* Requer mais recursos (CPU, memória, disco) para rodar.

***Container (Contêiner)***

* É um processo isolado que compartilha o kernel do sistema operacional do host.

* Cada contêiner é um processo isolado, com seu próprio namespace e isolamento de recursos.

* Não requer um hipervisor para rodar.

* O processo de criação e configuração de um contêiner é mais rápido e simples.

* Requer menos recursos (CPU, memória, disco) para rodar.

## Quais características de uma imagem e quais as características de um container

**Images**

Uma imagem possui todo o que é necessário para sua aplicação funcionar.

*CUT-DOWN OS*: dentro de uma imagem possui o sistema operacional

As bibliotecas necessárias para nossa aplicação funcionar

Variáveis de ambiente

**Container**

É um ambiente isolado do nosso sistema operacional

O container é considerado um processo que é executado dentro de uma máquina

- O container pode ser iniciado ou parado

## Container e containerização

Um container é uma instância em execução de uma imagem Docker.

Os containeres permitem empacotar a aplicação e suas dependências
em um ambiente isolado. Garantindo a consistência na execução
da aplicação em diferentes ambientes.

### Conclusão

Container é mais leve que uma Machine Virtual.

Se o nosso objetivo é transferir a minha aplicação para um ambiente de produção, o container é a escolha mais fácil e eficiente.
