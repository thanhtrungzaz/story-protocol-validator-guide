# story-protocol-validator-guide

System Specs
Hardware	Requirement
CPU	4 Cores
RAM	8 GB
Disk	200 GB
Bandwidth	10 MBit/s

wget https://story-geth-binaries.s3.us-west-1.amazonaws.com/story-public/story-linux-amd64-0.9.11-2a25df1.tar.gz
wget https://story-geth-binaries.s3.us-west-1.amazonaws.com/geth-public/geth-linux-amd64-0.9.2-ea9f0d2.tar.gz

tar -zxvf story-linux-amd64-0.9.11-2a25df1.tar.gz
tar -zxvf geth-linux-amd64-0.9.2-ea9f0d2.tar.gz

screen -S geth

cd geth-linux-amd64-0.9.2-ea9f0d2.tar.gz
./geth --iliad --syncmode full

crlt a d 

screen -S aliad

cd story-linux-amd64-0.9.11-2a25df1.tar.gz

./story init  --network iliad 

./story run  

if  you run as user not root so change your home path 

crtl a d 

waiting until your node full sync  then creat validator  

cd story-linux-amd64-0.9.11-2a25df1.tar.gz

./story validator export --export-evm-key

this give you private-key validator wallet  . import it to metamask to get address then use faucet https://faucet.story.foundation/

when you have token in your validator wallet you can creat your validator . beware gas  better to get 2-3 IP token faucet 

./story validator create --stake 1000000000000000000

if pass your validator will creat  like this 

Transaction hash: 0x36b95f6cf400202cf9aaa6fa71740f61d9bdfac4a15a48f81542f076e7830cb4
Explorer URL: https://testnet.storyscan.xyz/tx/0x36b95f6cf400202cf9aaa6fa71740f61d9bdfac4a15a48f81542f076e7830cb4
Transaction sent, waiting for confirmation...
Transaction confirmed successfully!
Validator created successfully!








