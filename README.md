# Postgre + pgAdmin4
Esse é um projeto demo para uso de Postgre com pgAdmin4 usando docker-compose

## Levantar os containeres
A partir da raiz do projeto, execute:
```bash
docker-compose up -d
```

## Verificar rede
Para confirmar que a rede *postgres-compose-network* foi criada
```bash
docker network ls
```

## Verificar containeres
```bash
docker-compose ps
```

## Teste do pgAdmin
Para acessar o pgadmin4 via browser basta acessar http://localhost:16543. Apartir dai basta utilizar o e-mail padrão e a senha configurada no docker-compose.

Ao criar a conexão para acesso à instância do PostgreSQL levar em conta as seguintes considerações:
* Em Host name/address informar o nome do container que corresponde à instância do PostgreSQL (postgres-compose);
* Em Port definir o valor 5432 (porta default de acesso ao container e disponível a partir da rede postgres-compose-network; não informar a porta em que o PostgreSQL foi mapeado no host);
* No atributo Username será informado o usuário default do PostgreSQL (postgres), bem como a senha correspondente em Password (Postgres2020!).

### Referencia
https://medium.com/@renato.groffe/postgresql-pgadmin-4-docker-compose-montando-rapidamente-um-ambiente-para-uso-55a2ab230b89
