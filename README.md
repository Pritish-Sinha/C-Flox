# Flox
Winner at Garuda Hack 3.0
![NFT display/minting page](/public/win.png?raw=true "NFT display/minting page")
## White-label NFT gallery

* Showcase, mint, sell, buy, and transfer NFTs
* ERC-721 smart contract
* Adheres to strict [NFT provenance best-practices](https://link.medium.com/LJjFKB999lb)
* SEO optimised responsive site
* Allows "lazy minting" (offer NFTs without pre-minting them; buyer pays gas to mint)
* Shows links to Opensea & Rarible for secondary sales
* Re-assignable role for catalog management
* Configurable revenue shares
* Configurable royalty
* Deployable on any EVM blockchain (Ethereum, Polygon, Arbitrum, etc)

### Example front page:

![NFT display/minting page](/public/front.png?raw=true "NFT display/minting page")

### Example catalog page:

![NFT gallery page](/public/catalog.png?raw=true "NFT gallery page")

### Example NFT item page:

![NFT display/minting page](/public/nft.png?raw=true "NFT display/minting page")

## Deployment

### Deploy the smart contract and create a catalog file. [more...](/smart-contract/)

#### Installation
```
npm install
npx hardhat test
```

#### Deploy
```
npx hardhat deploy --args ./delpoyment_args_testnet.js --network rinkeby 
```

#### Signature test
```
npx hardhat sign --wei 1000 --id 123 --uri ipfs://foo.bar/123 --contract <DEPLOYED_CONTRACT_ADDRESS>  --network rinkeby
```

#### Verify on Etherscan (or Polygonscan)
```
npx hardhat verify --network rinkeby --constructor-args delpoyment_args_testnet.js <DEPLOYED_CONTRACT_ADDRESS>
```

### Deploy the user-facing client application to a suitable host (eg Vercel.com). [more...](/client/)

#### Installation
```
npm install
npm run dev
```
