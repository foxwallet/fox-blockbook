# fox blockbook
* 安装 docker
* 安装依赖 `apt install build-essential git wget pkg-config lxc-dev libzmq3-dev \
  libgflags-dev libsnappy-dev zlib1g-dev libbz2-dev \
  liblz4-dev graphviz`

## 我们的部署方式
* 编译 `sudo make BASE_IMAGE=ubuntu:20.04`
* 只需要编译后的 build/blockbook 二进制，节点也用自己另行部署的，然后用 supervisor 启动 blockbook

## 官方的部署方式
* 编译 `make BASE_IMAGE=ubuntu:20.04 all-bsc`
* 给 `/opt/coins` 设置软链: `ln -s /data/coins/ /opt/coins`
* 重复两次: `apt install ./build/backend-bsc_1.10.8-26675454-satoshilabs-1_amd64.deb`
* `systemctl start backend-bsc.service`
* 重复两次: `apt install ./build/blockbook-bsc_0.3.5_amd64.deb`
* `systemctl start blockbook-bsc.service`