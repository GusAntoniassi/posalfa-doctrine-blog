# Trabalho Pós - Doctrine
Trabalho desenvolvido para a disciplina de Doctrine da Pós Graduação WebDev da Faculdade Alfa Umuarama.

Professor: Eduardo Bona

## Instalação

### Requisitos

- Docker

### Instalação

```
docker-compose up -d
docker-compose exec zf bash -c 'composer install'
```

### Rodando o projeto pela primeira vez

Para executar o projeto pela primeira vez é bom se certificar que a 
pasta data tem permissões de escrita e leitura e escrita

```
chmod -R 775 data/
```

Copie o arquivo de configuração e edite de acordo com sua configuração de banco de dados (está configurado para rodar com o Docker sem precisar de nenhuma alteração).

```
cp config/autoload/local.php.dist config/autoload/local.php
```

### Criar tabelas no banco:
```
docker-compose exec zf bash -c 'php vendor/bin/doctrine-module orm:schema-tool:update --force'
```

## Development Mode

Habilite o modo de desenvolvimento (apenas em ambiente de desenvolvimento)

```
docker-compose exec zf bash -c 'composer development-enable'
```
