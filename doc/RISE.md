

## RISE钱包运维手册
#### 源码：https://github.com/RiseVision/rise-node

#### （1）安装
```
export NETWORK="mainnet"
wget https://raw.githubusercontent.com/RiseVision/rise-build/master/scripts/install.sh
bash install.sh install -r ${NETWORK?} -u https://downloads.rise.vision/core/${NETWORK}/latest.tar.gz

cd rise
wget https://downloads.rise.vision/snapshots/${NETWORK?}/latest -O latestsnap.gz
./manager.sh restoreBackup latestsnap.gz

./manager.sh status
#./manager.sh stop node
#./manager.sh start node
#./manager.sh reload node

```


##### 安装加密包libsodium.so，放到 JAVA CLASSPATH中。
```
sudo apt-get install libsodium-dev
ln -s /usr/lib/libsodium.so /usr/local/lib/libsodium.so
```
###### 源码安装
```
wget https://download.libsodium.org/libsodium/releases/libsodium-1.0.18-stable.tar.gz
./autogen.sh
./configure
make && make install
```
