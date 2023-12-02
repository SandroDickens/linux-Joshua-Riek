# 1. clone源码
```shell
git clone --depth=1 -b linux-6.6.y https://github.com/SandroDickens/linux-rockchip-v6.git
```

# 2. config
```shell
touch .scmversion
make ARCH=arm64 CROSS_COMPILE=aarch64-linux-gnu- rockchip_linux_defconfig
```

# 3. 编译
## 3.1 编译成deb包
```shell
make KERNELRELEASE="$(make kernelversion)-rockchip" KBUILD_IMAGE="arch/arm64/boot/Image" CROSS_COMPILE=aarch64-linux-gnu- ARCH=arm64 -j "$(nproc)" bindeb-pkg
```
## 3.2 编译成二进制包
```shell
make ARCH=arm64 CROSS_COMPILE=aarch64-linux-gnu- Image modules dtbs -j$(nproc)
```
