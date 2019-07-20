Blog de Exemplo
==================================================

Este exemplo é baseado em "Hello World" desenvolvido em Zend 3 e demontra:

  * Integração do site com a biblioteca Doctrine
  * Usando EntityManager
  * Criando entidades
  * Criando e parametrizando propriedades
  * Definindo relacionamento entre entidades
  * Criando repositórios

## Instalação

### Requisitos

- php >= 7.*
- php-cli instalando (verificar php -v)
- composer instalado (verificar composer -v)
- mysql >= 5.6
- (opcional) phpmnyadmin
- (opciona)) mysql-client (verificar mysql -v)

### Baixando

```
mkdir projeto-base
git clone git clone https://github.com/alfa-eduardobona/using-zf3-book-samples.git projeto-base
cd projeto-base/blog
```

### Instalando

```
composer install
```

### Rodando o projeto

```
php -S localhost:9001 -t public
```

### Rodando o projeto pela primeira vez

Para executar o projeto pela primeira vez é bom se certificar que a 
pasta data tem permissões de escrita e leitura e escrita

```
chmod -R 775 data/
```

Copie o arquivo de configuração e edite de acordo com sua configuração de banco de dados.

```
cp config/autoload/local.php.dist config/autoload/local.php
```

Confira o seguinte:

- Se a conexão com banco de dados está funcionando (pode ser via phpmyadmin ou via comando mysql -h xxx -u xxx -p
- Se ainda não tiver criado uma base, crie-a com o nome que preferir (exemplo zf3_blog)
- Garanta que os dados de usuário e senha utilizados para conectar enxergam esta base

## Development Mode

Habilite o modo de desenvolvimento (apenas em ambiente de desenvolvimento)

```
composer development-enable
```

## Projeto Base

Este projeto é um fork do [repositório](https://github.com/olegkrivtsov/using-zf3-book-samples/tree/master/blog) com alterações pontuais como:

- definição dos tipos de dados (columns, tipos e tamanhos)
- remoção do suporte a migrations (que será adicionado em momento oportuno)
- correções em entidades

## License (original)

This code is provided under the [BSD-like license](https://en.wikipedia.org/wiki/BSD_licenses). 

## Contributing (original)

If you found a mistake or a bug, please report it using the [Issues](https://github.com/olegkrivtsov/using-zf3-book-samples/issues) page. Your feedback is highly appreciated.
