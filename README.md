# Node
Installing and running OID node.

# What is a node?
A node distributes the blockchain among the people who use the blockchain. 
The second feature of a node is that it verifies the transactions of a blockchain.

You can setup a node on your own VPS using the instructions below.

# How do I connect with a node?
You can manually connect to a node using the following instructions.

Close your OID wallet and create the file opioid.conf in the folder "%APPDATA%\Opioid\".
(If you have not downloaded your OID wallet, click here). 

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

6) Download the deamon file by going here

7) Extract the tar file using the following command.

8) tar -xzvf opioid-daemon-linux.tar.gz

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

*** If you get an error at this point, you may need to compile from source. ***









