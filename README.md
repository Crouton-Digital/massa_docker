### Massa: The Decentralized and Scaled Blockchain
Massa is a truly decentralized blockchain controlled by thousands of people. With the breakthrough multithreaded technology, we're set for mass adoption.

### Introduction
Massa is a new blockchain reaching a high transaction throughput in a decentralized network. Our research is published in this technical paper. It shows that throughput of 10'000 transactions per second is reached even in a fully decentralized network with thousands of nodes.

An easy-to-read blog post introduction with videos is written here.

We are now releasing the Massa testnet in this Gitlab repository, with its explorer available at https://test.massa.net.

### Testnet Incentives
As decentralization is our core value, we would like to help you start and run a Massa node. Running a node during the testnet phase also helps us find bugs and improve usability, so it will be rewarded with real Massa on mainnet launch.

The mechanics of those rewards are described in the Testnet rules.

### Buy VPS on Hetzner
You need buy VPS with size CPX31 (4 CPU, 8Gb, HDD 160) and Docker CE Image initialisation 
or Ubuntu and install first Docker engine use manual:  
https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04

### Fast start massa node  in Docker 
```
sudo -i
curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /bin/docker-compose
chmod +x /bin/docker-compose

cd /opt 
git clone https://github.com/CroutonDigital/massa_docker.git
cd massa_docker
edit docker-compose.yml for setup your strong password and TAG image version
docker-compose up -d 
```
for read logs 
``` 
cd /opt/massa_docker
docker-compose logs -f 
```

for start massa-client 
```
cd /opt/massa_docker
docker exec -it massa-node bash  
cd massa-client/
./massa-client  
```



