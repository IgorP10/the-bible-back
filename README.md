# TheBible

# Configurando ambiente de desenvolvimento

```bash
# Install docker & docker-compose
https://docs.docker.com/engine/install/
https://docs.docker.com/compose/install/

# Copie e edite(opcional) o arquivo .env
cp .env.example .env

# Rodar o docker-compose
docker-compose up -d

# Rodar o composer
docker-compose exec app composer install

# Rodar as migrations
docker-compose exec app php ./vendor/bin/doctrine-migrations migrate --all-or-nothing --no-interaction
```

## Extra

```bash
# Criar uma migration
docker-compose exec app php ./vendor/bin/doctrine-migrations generate

# Rodar método DOWN de uma migration
docker-compose exec app php ./vendor/bin/doctrine-migrations migrations:execute --down Migration\Migrations\Version20240904140239

# Limpar cache do composer
docker-compose exec app composer clear-cache
```