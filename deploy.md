# fox blockbook

## docker build
*  安装docker
* `make BASE_IMAGE=ubuntu:20.04 all-ethereum`

## install
* `apt install build-essential git wget pkg-config lxc-dev libzmq3-dev \
  libgflags-dev libsnappy-dev zlib1g-dev libbz2-dev \
  liblz4-dev graphviz`

* 给 `/opt/coins` 设置软链: `ln -s /data/coins/ /opt/coins`

* 重复两次: `apt install ./build/backend-ethereum_1.10.8-26675454-satoshilabs-1_amd64.deb`
* `systemctl start backend-ethereum.service`

* 重复两次: `apt install ./build/blockbook-ethereum_0.3.5_amd64.deb`
* `systemctl start blockbook-ethereum.service`