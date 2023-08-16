# Web3 PWA Boilerplate

A boilerplate for a web3 progressive web app.

Demo (use a mobile): https://jamesbachini.com/misc/pwa/

This was inspired by Friend.Tech and has the following UX flow:

1) Visit website and receives custom instructions on how to install app
2) User adds to home screen or installs app then opens using the icon
3) A new wallet address is generated and the user is prompted to fund using Goerli ETH
4) The balance is checked until it receives funds and is ready to go

User receives custom instructions based on their browser user agent which supports iPhone, iPad and Android as default. Installing a PWA directly from a site gets around the app store restrictions on payment commissions.

Ethers.js v6 is used alongside a custom RPC provider. This means no external wallet is required.

Currently the private key for the tmpWallet is stored in localStorage but this is likely insecure and there may be better methods of storing it locally.

Once the wallet is funded transactions can be signed using ethers and broadcast using the JSON RPC provider.

There are 3 key files:-
- index.html = welcome page with instructions on how to install
- app.html = main entry page for the dApp
- manifest.json = sets out default options and icons for the PWA