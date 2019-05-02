### Installation
#### 1. Install Docker (v17.03.1-ce or higher)
```sh
# Setup the repository
$ sudo apt-get update
$ sudo apt-get install apt-transport-https ca-certificates curl gnupg-agent software-properties-common
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
$ sudo apt-get update
$ sudo apt-get install docker-ce docker-ce-cli containerd.io

# To access as non-root user
$ sudo groupadd docker
$ sudo usermod -aG docker $USER
$ sudo usermod -aG docker www-data
$ docker run hello-world
```

#### 2. Install docker-compose (v1.9.0 or higher)
```sh
$ sudo apt install docker-compose
$ docker --version && docker-compose --version
# Make sure that you are running Docker version 17.03.1-ce, Docker Compose version 1.9.0 or higher
```

#### 3. Install Golang (v1.8 or higher required)
```sh
$ cd ~/Downloads
$ sudo curl -O https://dl.google.com/go/go1.12.4.linux-amd64.tar.gz
$ sudo tar -xvf go1.12.4.linux-amd64.tar.gz
$ sudo mv go /usr/local
$ echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.profile
$ source ~/.profile
$ go version
```

#### 4. Install Hyperledger Samples, Binaries and Docker Images and Clone Fabric-Samples
```sh
$ curl -sSL http://bit.ly/2ysbOFE | bash -s
$ cd ~/Desktop; mkdir -p oss2019/blockchain && cd oss2019/blockchain
$ git clone https://github.com/hyperledger/fabric-samples
$ go get -u github.com/hyperledger/fabric/core/chaincode/shim # you may have to wait sometime for this one
```