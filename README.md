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
docker-compose -f "docker-compose-dev.yml" up -d --build
```

## Kick start `saleor-platform`

```shell
cd $SALEOR_PLATFORM_PATH
docker-compose -f "docker-compose-dev.yml" up -d --build
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
