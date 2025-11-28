PoCWN Lab2
== 

install gtp5g

```bash
sudo apt -y update
sudo apt -y install gcc g++ cmake autoconf libtool pkg-config libmnl-dev libyaml-dev
cd gtp5g
make clean && make
sudo make install
```

run open5gc
```
cd base
git clone --recursive -j `nproc` https://github.com/free5gc/free5gc.git
cd ..

# Build image from local
sudo make

# amd64
sudo docker compose -f 314581029.yaml build
sudo docker compose -f 314581029.yaml up -d
```