<p align="center">
<img src="https://cwmkt.com.br/wp-content/uploads/2024/04/logo_github.png" width="240" />
<p align="center">Seja bem-vindo ao Guia de Instalação Chatwoot+Evolution+Typebot 🚀</p>
</p>
  
<p align="center">
<img src="https://whatsapp.com/favicon.ico" alt="WhatsAPP-logo" width="32" />
<span>Grupo WhatsaAPP: </span>
<a href="https://chat.whatsapp.com/K0HnkUZ41CYL8txpPWx2hO" target="_blank">Grupo</a>
</p>

<hr />
<hr />

Crie Projects

![48098512-1c18b7b28300a0bfa7a21c97deb109fe](https://github.com/cwmkt/easypanelevotypebot/assets/91642837/aaad7bdb-64f3-480f-a311-098fc3ca8220)


Adicione nome de Project

![48098522-0c485df00f5cadb0d329061c35fee46c](https://github.com/cwmkt/easypanelevotypebot/assets/91642837/b72c1359-91ca-4bf6-9fb1-32525ba5747b)

Clique na aba Templates

![48098535-90f9b4f370bb8b06cfd7e4acf0ee0f97](https://github.com/cwmkt/easypanelevotypebot/assets/91642837/03c1830c-621c-40b3-94ee-93eb568c8d2e)

Localize APP Chatwoot, clique nele

![48098554-b51ae806b9ed93f6a7b1cccc37ed62c8](https://github.com/cwmkt/easypanelevotypebot/assets/91642837/2d97bbb3-50c4-4e12-b87a-5673c14e7f23)

Nessa tela troque idioma e Imagem docker, clique me Create

![48098583-e5b73cced4eb56836a2b2c18645c442c](https://github.com/cwmkt/easypanelevotypebot/assets/91642837/2e88be4b-75bf-4b8e-810f-21db54c7b3a9)

```bash
chatwoot/chatwoot:latest
```

```bash
pt_BR
```

Clique em Go to Project

![48098610-7d30b35fd2e3b6dee2e329b957c726d7](https://github.com/cwmkt/easypanelevotypebot/assets/91642837/6e76a069-024e-4076-a082-1187efb825d9)

Clique Icone marcado no print abaixo e faça seu cadastro

![48098622-3c44bfa8fa7202daa7e9a93d14c0933a](https://github.com/cwmkt/easypanelevotypebot/assets/91642837/ad675e5e-b193-43b8-b4c0-fb7d57286c0b)

Agora vamos instalar a Evolution API precisamos do Mongo e do Redis

Agora vamos criar Mongo DB, adicione uma senha

![48098737-fc1b5ea237932133f199cca87d89567e](https://github.com/cwmkt/easypanelevotypebot/assets/91642837/073447d0-1bc7-4931-b112-2ef6eb678410)

![48098729-3a51b9f9b1eda910803a6218d8a99116](https://github.com/cwmkt/easypanelevotypebot/assets/91642837/451c70e0-a340-4851-b9bd-ecd68871fec9)

Na aba Credentials, vai ver os dados de seu banco, vamos precisar colocar essa informações nas variaveis nos passos mais frente

![48098751-dd47c59894708283e607955f17daa4be](https://github.com/cwmkt/easypanelevotypebot/assets/91642837/f72f00a6-ef75-4a46-bd8b-cfc708e6a472)

Agora vamos criar Redis, adicione uma senha

![48098771-97de83121e655c910b7e9a1cac3fcede](https://github.com/cwmkt/easypanelevotypebot/assets/91642837/20f865f9-bf9a-4678-aa85-f534bae61a21)

Na aba Credentials, vai ver os dados de seu redis vamos precisar colocar essa informações nas variaveis nos passos mais frente

![48098784-a2497979a82ebe27c36a82d3ca5562d8](https://github.com/cwmkt/easypanelevotypebot/assets/91642837/7b1225a1-9e48-42b0-a30a-3e3732ff26a9)

Clique na aba APP

Coloque nome evolution

![48098643-fa2a774a3ae6553fdff5d152b055fb2b](https://github.com/cwmkt/easypanelevotypebot/assets/91642837/c20e2289-3a6b-4522-a0ec-3ebb1cd6e70a)

![48098646-60fea078a1e05d065b1889647a0222b3](https://github.com/cwmkt/easypanelevotypebot/assets/91642837/e5dfccd1-a681-4646-ad9d-b128cbb78908)


Na aba abaixo clique em Docker Image e adicione Imagem abaixo, depois salve

```bash
docker pull atendai/evolution-api:latest
```

![48098680-cb32525d28f33a65a9085a8a006b6779](https://github.com/cwmkt/easypanelevotypebot/assets/91642837/95e6052e-8c1a-429a-b7ad-ee031b5954a5)

Em Environment adicione variaveis abaixo, e troque as senhas do Redis e Mongo

```bash
NODE_VERSION=20.7.0
YARN_VERSION=1.22.19
TZ=America/Sao_Paulo
DOCKER_ENV=true
SERVER_TYPE=http
SERVER_PORT=8080
SERVER_URL=https://dominioeasypanel.com
CORS_ORIGIN=*
CORS_METHODS=POST,GET,PUT,DELETE
CORS_CREDENTIALS=true
LOG_LEVEL=ERROR,WARN,DEBUG,INFO,LOG,VERBOSE,DARK,WEBHOOKS
LOG_COLOR=true
LOG_BAILEYS=error
DEL_INSTANCE=false
DEL_TEMP_INSTANCES=true
STORE_MESSAGES=true
STORE_MESSAGE_UP=true
STORE_CONTACTS=true
STORE_CHATS=true
CLEAN_STORE_CLEANING_INTERVAL=7200
CLEAN_STORE_MESSAGES=true
CLEAN_STORE_MESSAGE_UP=true
CLEAN_STORE_CONTACTS=true
CLEAN_STORE_CHATS=true
DATABASE_ENABLED=true
DATABASE_CONNECTION_URI=mongodb://mongo:senhamongo@evolutionapi-mongo:27017
DATABASE_SAVE_DATA_INSTANCE=true
DATABASE_SAVE_DATA_NEW_MESSAGE=false
DATABASE_SAVE_MESSAGE_UPDATE=false
DATABASE_SAVE_DATA_CONTACTS=false
DATABASE_SAVE_DATA_CHATS=false
RABBITMQ_ENABLED=false
RABBITMQ_MODE=global
RABBITMQ_EXCHANGE_NAME=evolution_exchange
RABBITMQ_URI=amqp://guest:guest@rabbitmq:5672
WEBSOCKET_ENABLED=false
WEBSOCKET_GLOBAL_EVENTS=false
WA_BUSINESS_TOKEN_WEBHOOK=evolution
WA_BUSINESS_URL=https://graph.facebook.com
WA_BUSINESS_VERSION=v18.0
WA_BUSINESS_LANGUAGE=pt_BR
SQS_ENABLED=false
SQS_ACCESS_KEY_ID=
SQS_SECRET_ACCESS_KEY=
SQS_ACCOUNT_ID=
SQS_REGION=
WEBHOOK_GLOBAL_URL=
WEBHOOK_GLOBAL_ENABLED=false
WEBHOOK_GLOBAL_WEBHOOK_BY_EVENTS=false
WEBHOOK_EVENTS_APPLICATION_STARTUP=false
WEBHOOK_EVENTS_INSTANCE_CREATE=false
WEBHOOK_EVENTS_INSTANCE_DELETE=false
WEBHOOK_EVENTS_QRCODE_UPDATED=true
WEBHOOK_EVENTS_MESSAGES_SET=true
WEBHOOK_EVENTS_MESSAGES_UPSERT=true
WEBHOOK_EVENTS_MESSAGES_UPDATE=true
WEBHOOK_EVENTS_MESSAGES_DELETE=true
WEBHOOK_EVENTS_SEND_MESSAGE=true
WEBHOOK_EVENTS_CONTACTS_SET=true
WEBHOOK_EVENTS_CONTACTS_UPSERT=true
WEBHOOK_EVENTS_CONTACTS_UPDATE=true
WEBHOOK_EVENTS_PRESENCE_UPDATE=true
WEBHOOK_EVENTS_CHATS_SET=true
WEBHOOK_EVENTS_CHATS_UPSERT=true
WEBHOOK_EVENTS_CHATS_UPDATE=true
WEBHOOK_EVENTS_CHATS_DELETE=true
WEBHOOK_EVENTS_GROUPS_UPSERT=true
WEBHOOK_EVENTS_GROUPS_UPDATE=true
WEBHOOK_EVENTS_GROUP_PARTICIPANTS_UPDATE=true
WEBHOOK_EVENTS_CONNECTION_UPDATE=true
WEBHOOK_EVENTS_LABELS_EDIT=true
WEBHOOK_EVENTS_LABELS_ASSOCIATION=true
WEBHOOK_EVENTS_CALL=true
WEBHOOK_EVENTS_NEW_JWT_TOKEN=false
WEBHOOK_EVENTS_TYPEBOT_START=false
WEBHOOK_EVENTS_TYPEBOT_CHANGE_STATUS=false
WEBHOOK_EVENTS_CHAMA_AI_ACTION=false
WEBHOOK_EVENTS_ERRORS=false
WEBHOOK_EVENTS_ERRORS_WEBHOOK=
CONFIG_SESSION_PHONE_CLIENT=EvolutionAPI
CONFIG_SESSION_PHONE_NAME=Chrome
QRCODE_LIMIT=30
QRCODE_COLOR=#198754
TYPEBOT_API_VERSION=latest
CACHE_REDIS_ENABLED=true
CACHE_REDIS_URI=redis://default:senharedis@evolutionapi-redis:6379
CACHE_REDIS_PREFIX_KEY=evolution
CACHE_REDIS_TTL=604800
CACHE_REDIS_SAVE_INSTANCES=false
CACHE_LOCAL_ENABLED=false
CACHE_LOCAL_TTL=604800
AUTHENTICATION_TYPE=apikey
AUTHENTICATION_API_KEY=B6D711FCDE4D4FD5936544120E713976
AUTHENTICATION_EXPOSE_IN_FETCH_INSTANCES=true
AUTHENTICATION_JWT_EXPIRIN_IN=0
AUTHENTICATION_JWT_SECRET=L=0YWt]b2w[WF>#>:&E`
AUTHENTICATION_INSTANCE_MODE=server
AUTHENTICATION_INSTANCE_NAME=evolution
AUTHENTICATION_INSTANCE_WEBHOOK_URL=<url>
AUTHENTICATION_INSTANCE_CHATWOOT_ACCOUNT_ID=1
AUTHENTICATION_INSTANCE_CHATWOOT_TOKEN=123456
AUTHENTICATION_INSTANCE_CHATWOOT_URL=<url>
```

![48098698-f2253d35287f26f70eba1a6c02563179](https://github.com/cwmkt/easypanelevotypebot/assets/91642837/f2aae6ff-abbd-4a4a-9610-a2fea92c1f82)

