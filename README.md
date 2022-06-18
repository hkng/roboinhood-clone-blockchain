## Roboinhood clone blockchain


## Sanity
    https://www.sanity.io/
    cd studio
    npm install -g @sanity/cli
    sanity init --coupon cleverprogrammer

    create schema under studio/schemas
    sanity start

    create .env
    SANITY_PROJECT_ID = xxxx
    SANITY_TOKEN = yyyy

## Moralis
   https://www.moralis.io
   npm install react-moralis
   npm install moralis

## Netlify

## Tailwind 
   npm install -D tailwindcss postcss autoprefixer
   npx tailwindcss init -p

   edit tailwind.config.js and replace following configuration
            module.exports = {
                content: [
                    './pages/**/*.{js,ts,jsx,tsx}',
                    './components/**/*.{js,ts,jsx,tsx}',
                ],
                theme: {
                    extend: {},
                },
                plugins: [],
                }

    edit styles/globals.css and add following css library
        @tailwind base;
        @tailwind components;
        @tailwind utilities;

## React
   npm install react-icons
   npm install react-chartjs-2
   npm install @sanity/client
   npm install axios

## Web 3 library
    npm install @web3auth/web3auth magic-sdk @magic-sdk/types @walletconnect/web3-provider

## Environment variable
   Create .env file as below
        SANITY_PROJECT_ID = y9u9wurs
        SANITY_TOKEN = 
        NEXT_PUBLIC_MORALIS_SERVER_URL =
        NEXT_PUBLIC_MORALIS_APP_ID = 
        MORALIS_MASTER_KEY = 
        ALCHEMY_API_URL = 
        WALLET_PRIVATE_KEY =
        COIN_RANKING_HOST =
        COIN_RANKING_KEY =
    
    Remark: NEXT_PUBLIC_ prefix is used by Next.js

    Use environement variable (e.g)
     process.env.SANITY_PROJECT_ID

    Files on the left have more priority than files on the right:

        npm start: .env.development.local, .env.local, .env.development, .env
        npm run build: .env.production.local, .env.local, .env.production, .env
        npm test: .env.test.local, .env.test, .env (note .env.local is missing)

## Setup hardhat
   cd smart-contract
   npx hardhat
    > Create a basic sample project
    select smart-contract folder
    
    npm install @openzeppelin/contracts dotenv @nomiclabs/hardhat-waffle chai ethereum-waffle ethers hardhat

    update hardhat.config.js

## Setup Alchemy
   https://www.alchemy.com/

   login and create new project called 
    roboinhood-clone-blockchain

   cd smart-contract
   create .env with your ALCHEMY API and RINKEBY private key
     ALCHEMY_API_URL =
     RINKEBY_PRIVATE_KEY = 

   npx hardhat run scripts/deploy.js --network rinkeby

   Markdown the contract address of each coin
        Dogecoin deployed to: 0xb633f55f9e03267800f827B319075604FFC069b9
        LinkToken deployed to: 0x98091c2EE3C68eD2e6A1Cb285040D69341f4855c
        DaiToken deployed to: 0xB84f33d8a6e0FCd63AD7877CBc5CD24ce46268BA
        UsdcToken deployed to: 0x4fcfF24771fAd0447FD7183De9AA3e17756A36e9
   
## Rinkeby test blockchain network
   Get testing etherum token
   https://faucets.chain.link/rinkeby

## smart-contract deployment
    cd smart-contract   
    npx hardhat run scripts/deploy.js --network rinkeby

    TINDER CONTRACT ADDRESS:  0x8bd5E9363c68c405105383e00c713D0b2eBC6B58

    update Contract address at lib/constants.js

    copy smart-contract/artifacts/contracts/TinderERC721.json to lib/TinderERC721.json folder

## RapidAPI - Coin Ranking API
    https://rapidapi.com

    update .env
    COIN_RANKING_HOST=coinranking1.p.rapidapi.com
    COIN_RANKING_KEY=

## Shortcut (with ES7+ React Snippets)
   Create Components - rafce
## Reference
https://www.youtube.com/watch?v=iMst9GE8wIM&t=1051s
