# 0. download an generic arm architecture toolchains
 
# 1. build kernel
 
## cd kernel path
cd kernel
 
## generate configs
cp arch/arm/configs/defconfig .config
make menuconfig
 
## compile with prebuilts toolchains
make -jN ARCH=arm CROSS_COMPILE=${CROSS_COMPILE}
