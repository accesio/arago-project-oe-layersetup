## Setup build (one time operation)

```sh
$./oe-layertool-setup.sh -f configs/processor-sdk/processor-sdk-09.01.00-config.txt
```

## Build the image
```sh
$cd build
/build$source conf/setenv 
/build$MACHINE=am64xx-evm bitbake acces-enet-min-image
```

## flash image to sd card
```sh
sudo bmaptool copy deploy-ti/images/am64xx-evm/acces-enet-min-image-am64xx-evm.wic.xz /dev/sda 
```
