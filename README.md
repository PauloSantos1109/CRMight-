# CRM System

Este projeto é um sistema CRM (Customer Relationship Management) desenvolvido utilizando **Nest.js** no backend e **Nuxt.js** no frontend. O sistema gerencia interações com clientes, integra-se com serviços de mensageria e utiliza uma estrutura de containers para garantir escalabilidade e fácil gerenciamento.

## Tecnologias Utilizadas

- **Backend:** [Nest.js](https://nestjs.com)
- **Frontend:** [Nuxt.js](https://nuxtjs.org)
- **Banco de Dados:** [PostgreSQL](https://www.postgresql.org)
- **Message Broker:** [RabbitMQ](https://www.rabbitmq.com)
- **Logs e Monitoramento:** [Elastic Stack](https://www.elastic.co/what-is/elk-stack) (Elasticsearch, Logstash, Kibana)
- **Containers:** [Docker](https://www.docker.com)
- **Load Balancer:** [Nginx](https://nginx.org)

## Requisitos

Para rodar este projeto, você precisará ter as seguintes dependências instaladas:

- [Docker](https://docs.docker.com/get-docker/) - Para gerenciar os containers.
- [Docker Compose](https://docs.docker.com/compose/install/) - Para orquestrar os containers.
- [Node.js](https://nodejs.org) - Para rodar scripts localmente (use [asdf](https://asdf-vm.com/) ou [nvm](https://github.com/nvm-sh/nvm) para gerenciar versões).
- [Yarn](https://yarnpkg.com/) ou [npm](https://www.npmjs.com/) - Para gerenciar pacotes do Node.js.

## Configuração do Ambiente

### Passo a Passo

1. **Clone o repositório:**

   Primeiro, clone o repositório em sua máquina:

   ```bash
   git clone https://github.com/seuusuario/seu-repositorio.git
   cd seu-repositorio



## Instalação das Dependências

```bash
    ### Backend (Nest.js)
    cd backend
    yarn install
    # ou
    npm install
```
    ### Frontend (Nuxt.js)

    Para instalar as dependências do frontend, execute:
    
    cd frontend
    yarn install
    # ou
    npm install
```


## Configuração das Variáveis de Ambiente

Crie os arquivos `.env` a partir dos exemplos e preencha com as variáveis necessárias:

```env
    POSTGRES_USER=<seu_usuario>
    POSTGRES_PASSWORD=<sua_senha>
    POSTGRES_DB=<seu_banco>´
```

## Inicie os Containers

Rode o comando abaixo para iniciar todos os containers (backend, frontend, banco de dados, etc.):

```bash
docker-compose up -d
```

No backend, execute as migrations do Prisma para garantir que o banco de dados esteja configurado corretamente:

```bash
cd backend
yarn prisma migrate dev
# ou
npm run prisma migrate dev
```

### Acesso aos Serviços
- Backend API: [http://localhost:3000/api](http://localhost:3000/api)
- Frontend: [http://localhost:3001](http://localhost:3001)
- Kibana (logs): [http://localhost:5601](http://localhost:5601)

### Estrutura do Projeto
A estrutura do projeto é organizada da seguinte forma:

``` bash
├── backend
│   ├── src              # Código-fonte do Nest.js (API e lógica de negócios)
│   ├── test             # Testes do backend
│   ├── prisma           # Configurações do Prisma
│   └── ...Markdown Preview Enhanced.
├── frontend
│   ├── assets           # Assets do Nuxt.js (imagens, fontes, etc.)
│   ├── components       # Componentes reutilizáveis do frontend
│   ├── layouts          # Layouts do Nuxt.js
│   └── ...
├── docker-compose.yml    # Configuração dos containers e orquestração
└── nginx
    └── nginx.conf       # Arquivos de configuração do Nginx
```
### TestesMarkdown Preview Enhanced.Markdown Preview Enhanced.
#### Backend

Para rodar os testes do backend, execute:

```bash
cd backend
yarn test
# ou
npm test
```