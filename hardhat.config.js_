require("@nomicfoundation/hardhat-toolbox");

/** @type import('hardhat/config').HardhatUserConfig */
module.exports = {
solidity: {
    compilers: [
      {
        version: "0.8.17",
		settings: {},
      },
      {
        version: "0.6.8",
		settings: {},
      },
      {
        version: "0.4.24",
      },
      {
        version: "0.5.0",
      },
    ],
},
  defaultNetwork: 'hardhat',
  networks: {
	  hardhat: {
		  forking: {
			  url: "https://eth-mainnet.g.alchemy.com/v2/<PUT YOUR API KEY HERE>"
		  }
	  }
  },
};
