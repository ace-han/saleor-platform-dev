# saleor-platform-dev

docker compose wrapper to run saleor-platform

## Check out `saleor-platform`

```shell
git clone https://github.com/mirumee/saleor-platform
```

## Copy customized files to target places respectively

```shell
# export SALEOR_PLATFORM_PATH=PATH_TO_saleor-platform
cd saleor-platform-dev
cp -r saleor/* $SALEOR_PLATFORM_PATH/saleor/
cp -r saleor-platform/* $SALEOR_PLATFORM_PATH/
```

## Kick start `saleor-platform`

```shell
cd $SALEOR_PLATFORM_PATH
docker-compose -f "docker-compose-dev.yml" up -d --build
```

## Init demo data

```shell
# refer to https://docs.saleor.io/docs/developer/installation

# login your `saleor` docker container
docker exec -it $SALEOR_CONTAINER_ID bash
python manage.py migrate
python manage.py collectstatic --noinput
python manage.py populatedb

# create your own admin
python manage.py createsuperuser

```

## Using `saleor-platform`

```shell
# storefront
open http://localhost:3000

# dashboard
open http://localhost:3000

# api
# launch `Remote Django App` in vscode to start debugging
```
