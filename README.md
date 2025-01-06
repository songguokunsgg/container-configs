# 一些常用的容器配置

通过这种方法避免安装繁重的虚拟机

podman 对于 Clash 的支持也比较方便

## 详细说明

- rk3568:

正点原子 RK3568 开发板编译环境

base: ubuntu22.04

- openwrt:

OpenwRT 编译环境

base: ubuntu22.04

## 使用说明

先依据自己项目情况配置 Containerfile 和 podman-compose.yml

构建镜像，这一步需要确保网络配置正常

```
podman build -t {your-image-name} -f Containerfile
```

构建镜像，这一步需要确保网络配置正常

然后通过 podman-compose 构建容器，yaml文件中的镜像名称需要与上一步保持一致

```
podman-compose up -d
``` 

即可
