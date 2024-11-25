
# Chat bot ágape 

Um Chat bot integrado ao whatsapp, que ao obter os dados do cliente, o envia um documento dam (contracheques, etc). 

## Stack utilizada

**Docker:** 
Plataforma para criar e gerenciar contêineres, facilitando a portabilidade de aplicativos.

**Traefik:** Roteador de aplicações que gerencia tráfego de microserviços, com balanceamento de carga e TLS automático.

**Portainer:** Interface web para gerenciar contêineres Docker de forma simples e intuitiva.

**Redis:** Banco de dados em memória, chave-valor, usado para caching e gerenciamento de sessões.

**Postgres:** Banco de dados relacional open-source, conhecido pela robustez e suporte a transações.

**Evolution-api:** API de controle de WhatsApp baseada no CodeChat, utilizando a biblioteca Baileys.

**TypeBot:** Ferramenta para criar chatbots com tipagem estática, facilitando o desenvolvimento.
## Funcionalidades

- Chat Automatizado
- Redirecionamento para um atendente humano
- Envio de documentação automatizada 
- Integração com sistema da prefeitura 



## Instalação da API

### Instalação Evolution V2 ###

sudo apt-get update ; apt-get install -y apparmor-utils

hostnamectl set-hostname manager2

Altera localhost para

nano /etc/hosts

127.0.0.1 manager1

curl -fsSL https://get.docker.com | bash

docker swarm init

docker network create --driver=overlay network_public

nano traefik.yaml

docker stack deploy --prune --resolve-image always -c traefik.yaml traefik


### Instalação portainer ###

nano portainer.yaml

docker stack deploy --prune --resolve-image always -c portainer.yaml portainer

portainer.chatbot.agapesistemas.com.br



### Documentação API ###

https://www.postman.com/agenciadgcode/evolution-api/collection/gqr041s/evolution-api-v2-0-7-release-candidate

### Repositorio Docker Hub ####

https://hub.docker.com/r/atendai/evolution-api/tags
## Integração API com whatsapp 

### Criação de instância ###

- Cria uma instância dentro da evolution-API, ultilizando baileys
- Conecta a instância com o whatsapp, através de um qrcode gerado
- Integra com softwares externos que a própria evolution possibilita (typebot, n8n, etc.)
## Fluxo do chat

### link de acesso : ###
https://app.typebot.io/typebots/cm27tp6xp00039gi81yc5exmy/edit
## Executável 

### Número com chat hospedado ###
+55 47 997352787
