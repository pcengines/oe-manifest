# WARNING

This was WIP repo and is not currently developed. It is not expected to work
correctly. If you have use-cases for such thing to be developed, please submit
an issue or PR with description of your needs / fixes.

# oe-manifest

OpenEmbedded (Yocto) repo manifest

## Init repositories

```
repo init -u git@github.com:pcengines/oe-manifest.git -b master
repo sync
```

## Prepare build configuration

```
cd poky
./yocto-docker/docker-bake.sh
cp meta-pcengines/example/local.conf.example build/conf/local.conf
cp meta-pcengines/example/bblayers.conf.example build/conf/bblayers.conf
sed -e "s@POKY_DIR@$PWD@g" -i ./build/conf/bblayers.conf
```

## Build

```
./yocto-docker/docker-bake.sh core-image-minimal
```
