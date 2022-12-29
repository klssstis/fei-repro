# fei-repro
Repro of FEI protocol hack -- thanks Immunefi, Lucash-dev, Pepin, Faith for your assistance in figuring out the interfaces

My goal was to learn about forking the mainnet, and reproducing an exploit -- I landed upon the article written by Lucash-dev for Immunefi, note that it was published in June 2021.

Link: https://medium.com/immunefi/a-guide-to-reproducing-ethereum-exploits-fei-protocol-224b30b517d6

I was following this article step-by-step, but within a few steps was already having an issue -- technology moves quickly, and even a little more than a year is an eternity when it comes to web3 and its tools.  Hardhat changed its wizard and sample files, and for getting the exploit to run, it became an increasingly difficult task.

I wrote an article about it, after spending hours and not able to get it to run.

Link: https://medium.com/@Brian.IsMeta/difficulty-of-reproducing-old-exploits-a613da2c2143

I reached out to Immunefi on Discord to get some assistance, and Pepin and Faith helped guide me on the path, and I worked on getting the other ones into the script, removing all the clutter of unneeded code / functions.  

Please note that the interfaces I include here are VERY trimmed down -- they are not the actual full interfaces, I only included function prototypes for things that are actually called by the exploit code!!!!!

I hope this is helpful for anyone trying to run this exploit.
