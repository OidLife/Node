# Node
Installing and running OID node.

# What is a node?
A node distributes the blockchain among the people who use the blockchain. 
The second feature of a node is that it verifies the transactions of a blockchain.

You can setup a node on your own VPS using the instructions below.

# How do I connect with a node?
You can manually connect to a node using the following instructions.

Close your OID wallet and create the file opioid.conf in the folder "%APPDATA%\Opioid\".
(If you have not downloaded your OID wallet, go here -> https://github.com/OidLife/Wallets). 

Paste the following text into opioid.conf and save the file.

addnode=REPLACE_WITH_YOUR_VPS_IP_OR_HOSTNAME

Replace the text "REPLACE_WITH_YOUR_VPS_IP_OR_HOSTNAME" with an IP address or hostname. 

E.G. addnode=37.97.242.80 or addnode=node.myvpshostname.com

# How do I setup a node on Ubuntu server?
You can setup a node on Ubuntu server using the following instructions.

Rent a VPS or droplet from Digital Ocean running Ubuntu 14.04 server.
(You can install this with Ubuntu 16.04+ but you may encounter some troubleshooting).

# Update your VPS using the following commands.

1) sudo apt-get update

2) sudo apt-get upgrade

# Install the necessary dependencies using the following commands.

3) sudo apt-get install build-essential libssl-dev libdb-dev libdb++-dev libboost-all-dev git libssl1.0.0-dbg

4) sudo apt-get install libdb-dev libdb++-dev libboost-all-dev

5) sudo apt-get install libminiupnpc-dev libminiupnpc-dev libevent-dev libcrypto++-dev libgmp3-dev

6) Download the daemon file by going to -> https://oid.life/node/opioid-daemon-linux.tar.gz

7) Extract the tar file using the following command.

8) tar -xzvf opioid-daemon-linux.tar.gz
(You can remove the tar file by using ```rm opioid-daemon-linux.tar.gz```)

# Install the daemon.

9) chmod +x opioidd

10) sudo mv opioidd /usr/bin/

# Create the config file.

11) cd ~

12) mkdir .opioid

13) cd .opioid 

14) opioid.conf

# Paste the following lines in opioid.conf.

```
rpcuser=RPC_USERNAME
rpcpassword=RPC_PASSWORD
rpcallowip=127.0.0.1
listen=1
server=1
txindex=1
daemon=1
```

# Start your node with the following command.

opioidd

*** If you get an error running the daemon node at this point, you may need to compile from source. ***
(Go here to -> https://github.com/OidLife/Compiling)

# How do I setup a node on Windows server?
You can setup a node on Windows server using the following instructions.

1) Download the Windows QT wallet by going to -> https://github.com/OidLife/Wallets
(Upload the file to your Windows server.)

2) Extract the zip file opioid-qt.zip.

3) Close your wallet and create the file opioid.conf in the folder "%APPDATA%\Opioid\".

4) Paste the following text into opioid.conf and save the file.

```
rpcuser=rpc_examplecoin
rpcpassword=69c863e3356d3dae95df454a1
rpcallowip=127.0.0.1
listen=1
server=1
txindex=1
```
Your wallet will now act as a node when you start your wallet.

*** If you encounter errors opening you wallet, check your opioid.conf file. ***
*** If you continue with wallet errors, do the following: ***

1) Backup your wallet.dat file to a cold storage location. 
2) Delete all folders and files in "%APPDATA%\Opioid\".
3) Delete any instance of Opioid qt. 
4) Re-download Opioid Windows wallet and install. 
5) Place your earlier backup of wallet.dat file back in "%APPDATA%\Opioid\".
6) Run your Opioid wallet. 

Thank you,
OID Team










