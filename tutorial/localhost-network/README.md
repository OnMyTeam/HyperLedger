## hyperledger v2.2 localhost network ����

�����۷��� v2.2�� Ȱ���Ͽ� ���� host���� �������� �����̳ʷ� ��Ʈ��ũ�� ������.<br>
<img src="images/image3.jpg" alt="drawing" width="450"/><br>
* Operating system: 18.04.02 LTS live-server
* Go version: 1.14
* NodeJS version: 12.18.3
* NPM version: 6.14.6
* Channel: mychannel
* Organization: Org1, Org2, Org3
* CA: 1��(Org1)
* DB: CouchDB
* TLS: false
* Consensus Type: Solo

## 1. Docker ��ġ

```
$ sudo apt install docker.io
$ sudo apt install docker-compose
$ sudo apt install software-properties-common
$ sudo usermod -aG docker $USER
$ sudo reboot
$ docker version 

```
<img src="images/image1.png" alt="drawing" width="450"/><br>

## 2. nodeJS ��ġ

```
$ sudo apt-get update 
$ sudo apt-get install build-essential libssl-dev
$ curl -sL http://raw.githubusercontent.com/creationix/nvm/v0.31.0/install.sh -o install_nvm.sh
$ bash install_nvm.sh 
$ source ~/.profile
$ sudo reboot
$ nvm install v12.18.3
$ node -v
$ npm -v 
```
<img src="images/image2.png" alt="drawing" width="450"/><br>

## 3. Hyperledger fabric samples v2.2 ��ġ
```
$ mkdir -p $HOME/go/{src,pkg,bin}
$ cd ~/go/src
$ curl -sSL http://bit.ly/2ysbOFE | bash -s -- 2.2.0 1.4.7
$ sudo apt install vim
$ sudo vim ~/.profile
  �Ʒ� �����Ͽ� ȯ�溯�� ���
$ source ~/.profile
```
<img src="images/image4.png" alt="drawing" width="450"/><br>
## 4. localhost-network ���丮 �̵�
�ٿ� ���� localhost-network ���丮�� ��ġ�� fabric-samples ���丮�� �̵� ��Ŵ.<br>
����, fabric-samples ���丮���� �۾� ����
```
$ mv $HOME/hyperledger/tutorial/localhost-network/ $HOME/go/src/fabric-samples/
$ cd $HOME/go/src/fabric-samples
```

## 5. ��Ʈ��ũ ���� �� Ȯ��
### 5.1 localhost-network directory ��������
* application: hyperledger network ���� �� admin, user ���
* contract: chaincode(fabcar)
* network: ��Ʈ��ũ ����
<br>
<img src="images/image5.png" alt="drawing" width="450"/><br>

### 5.2 ��Ʈ��ũ ������ ���� ���� �۾�
* Peer, Orderer�� MSP ���� �� genesis block ����.
* �̶� CA�� Org1�� CA�� �ǹ���.
* ������ �ǽ��� ���� Org1���� CA�� ���� �Ͽ�����, �� Org�� CA������ �����ϴ� ���� ����.
```
$ cd $HOME/go/src/faric-samples/localhost-network/network
$ ./generate.sh
```
<img src="images/image6.PNG" alt="drawing" width="700"/><br>

### 5.3 ��Ʈ��ũ ���� 
* Peer, Orderer, CA �����̳� ����
* mychannel ����
* �� Org�� Peer�� mychannel ����
* �� Org�� AnchoPeer ������Ʈ
```
$ cd $HOME/go/src/faric-samples/localhost-network/network
$ ./start.sh
$ docker ps -a
```
<img src="images/image7.PNG" alt="drawing" width="700"/><br>
<img src="images/image8.PNG" alt="drawing" width="700"/><br>

## 6. ü���ڵ� ��ġ
* ��Ű¡(packaging)
* �� Org�� Peer�� ��ġ(install)
* �� Org�� Peer�� definition ����(approve)
* Ŀ��(commit)
```
$ cd $HOME/go/src/faric-samples/localhost-network/network
$ ./deployCC.sh
```
<img src="images/image9.PNG" alt="drawing" width="700"/><br>
<img src="images/image10.PNG" alt="drawing" width="700"/><br>