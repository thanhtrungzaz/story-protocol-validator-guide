# story-protocol-validator-guide

System Specs

Hardware	Requirement

CPU	4 Cores

RAM	8 GB

Disk	200 GB

Bandwidth	10 MBit/s
```bash
wget https://story-geth-binaries.s3.us-west-1.amazonaws.com/story-public/story-linux-amd64-0.9.11-2a25df1.tar.gz
```
```bash
wget https://story-geth-binaries.s3.us-west-1.amazonaws.com/geth-public/geth-linux-amd64-0.9.2-ea9f0d2.tar.gz
```
```bash
tar -zxvf story-linux-amd64-0.9.11-2a25df1.tar.gz
```
```bash
tar -zxvf geth-linux-amd64-0.9.2-ea9f0d2.tar.gz
```
```bash
screen -S geth
```
```bash
cd geth-linux-amd64-0.9.2-ea9f0d2
```
```bash
./geth --iliad --syncmode full
```
crlt a d 
```bash
screen -S aliad
```
```bash
cd story-linux-amd64-0.9.11-2a25df1
```
```bash
./story init  --network iliad
```
```bash
./story run  
```
if  you run as user not root so change your home path 

crtl a d 

waiting until your node full sync  then creat validator  
```bash
cd story-linux-amd64-0.9.11-2a25df1.tar.gz
```
```bash
./story validator export --export-evm-key --evm-key-path .env
```

this give you private-key validator wallet  . import it to metamask to get address then use faucet https://faucet.story.foundation/

when you have token in your validator wallet you can creat your validator , gas . better to faucet 2-3 IP token 
```
./story validator create --stake 1000000000000000000
```

if pass your validator will creat  like this 


```
Transaction hash: 0x36b95f6cf400202cf9aaa6fa71740f61d9bdfac4a15a48f81542f076e7830cb4

Explorer URL: https://testnet.storyscan.xyz/tx/0x36b95f6cf400202cf9aaa6fa71740f61d9bdfac4a15a48f81542f076e7830cb4

Transaction sent, waiting for confirmation...

Transaction confirmed successfully!

Validator created successfully!
```







