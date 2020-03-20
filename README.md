# Masternode Update 1005 
	

# LOGIN in your node via Putty! 

```bash
ozeety-cli stop
```
```bash
sudo wget https://github.com/Flashgroupdevs/Linux_wallet/raw/master/Linux-Wallet-16.04/ozeetyd
```
```bash
sudo wget https://github.com/Flashgroupdevs/Linux_wallet/raw/master/Linux-Wallet-16.04/ozeety-tx
```
```bash
sudo wget https://github.com/Flashgroupdevs/Linux_wallet/raw/master/Linux-Wallet-16.04/ozeety-cli
```
Permissions:
```bash
 chmod 777 *
```

```bash
sudo mv ozeetyd ozeety-cli ozeety-tx /usr/bin/
```
```bash
cd .ozeety
```
```bash
rm -R -f chainstate blocks .log mn.dat budget.dat peers.dat  mncache.dat mnpayments.dat fee_estimates.dat db.log debug.log database/ backups/ ozeety.pid .lock
```
Get chain 
```bash
sudo wget https://github.com/Flashgroupdevs/OZEETY_chain-v2/raw/master/Archive.zip
```
```bash
chmod 777 *
```
```bash
unzip OZEETY_chain-v2/Archive.zip
```

```bash
chmod 777 *
```

```bash
cd ~/
```
restart
```bash
ozeetyd 
```


to check if you are on the correct chain: 
on the wallet: in debug console type in: 
```bash
getblockhash 327271
```
Output should be: 
36c8d26bb92f04d814118c6f90d55c3c27eece95a4a19c70139ecac988d79a89


to check for the correct chain on the node: 
check in putty as the user you setup the node: 
```bash
./ozeety-cli getblockhash 327271
```
should be the same output:
36c8d26bb92f04d814118c6f90d55c3c27eece95a4a19c70139ecac988d79a89
