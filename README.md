# Nimble Miner Setup Guide
Welcome to the Nimble Miner setup guide. This document is designed to help you get started with the Nimble Miner. I've structured this guide to make the setup process as straightforward as possible.

# Introduction
Nimble Miner allows users to contribute to the Nimble network by performing AI inference tasks in exchange for rewards. This guide will take you through the necessary steps to set up your mining operation.

For curious readers to learn more about how to start please read it first [https://discord.com/channels/1139328143400894604/1165053157391478825/1225876548255744121](https://discord.com/channels/1139328143400894604/1256018146561757184/1256021479385071658)

# System Specifications
``` Linux OS
Nvidia GPU with Cuda
4GB RAM
1 GB disk space 
GNU LIBC >= 2.34
```
# Rent GPUs
This guidline working good with **Cuda:12.0.1-Devel-Ubuntu22.04** template for only one times to copy and paste
![image](https://github.com/b5prolh/nimble-miner-public/assets/18376326/b1e13f1b-3c6d-46f8-8862-95676717841a)

If this is first time you use vast and dont know how to connect, please see it first: https://www.youtube.com/watch?v=KraLVgFS4vU

For cheapest price, using gpus that rent on [CLORE](https://clore.ai?ref_id=sblcyoxd) is the good choice. In this tutorial, I will using gpus that rent on clore.

# GENERATE NIMBLE WALLET
SKIP THIS STEP IF U ALREADY HAVE WALLET

## Install wallet cli
``` 
git clone https://github.com/nimble-technology/wallet-public.git && cd wallet-public && make install
```
## Create wallet
```
cd && cd wallet-public ./nimble-networkd keys add YOUR_WALLET_NAME
```
After you've entered your passphrase, your wallet shoud be successfully created and the “address: nimblexxxx” output can confirm that!
Copy the generated Nimble address and save your wallet information in a safe place.

# RUN NIMBLE MINING
## upgrade GNU LIBC >= 2.34
```
sudo apt update && sudo apt upgrade -y && sudo apt dist-upgrade -y && sudo apt install curl && sudo apt-get install -y libcurl4-openssl-dev && sudo apt install -y update-manager-core && sudo do-release-upgrade -f DistUpgradeViewNonInteractive
```
After run success, run 
```
ldd --version
```
the ldd version should >= 2.34

![image](https://github.com/user-attachments/assets/f6cd0efb-8f68-401d-8fd2-4ca97e01929f)


## Create serivce config file
```
sudo mkdir -p /etc/nimbleservice && sudo echo "NIMBLE_PUBKEY=YOUR_WALLET_ADDRESS" | sudo tee /etc/nimbleservice/nimbleservice.conf
```

## Clone nimble project
```
git clone https://github.com/nimble-technology/nimble-miner-public.git
```

## Run mining
```
cd nimble-miner-public && chmod +x nimbleminer && ./nimbleminer
```

# Contact
you can contact me if have any issue related this guideline
Discord: mytt0918
[Telegram](https://t.me/OxCaos)
[Twitter](https://twitter.com/kiwigamefi)


# Donate
If u want invite me a starbuck, give it to: 

TRC20 
``` 
TQe1d7nZq3E3T3b6FsU5E5VeapNGVBeB18
 ```
BEP20 
``` 
0xf96bbf1532287fb309409dbc4e6491eae46c030a
 ```
Sol 
```
7ixWCfwk3xVoYkr2utfCkdqG3cVcUTJQ8cZJmpioGH5g 
```

Many thanks and hope we will become richer by mine NIM
