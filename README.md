# Blockchain-Communication-System
  
  Secure DApp – Encrypted Messaging + IPFS Storage + Smart Contract Identity System
  Secure Encrypted Messaging DApp

## A fully decentralized application where users can:

✔ Generate public/private RSA key pairs

✔ Register their public key on the blockchain

✔ Encrypt messages using recipient public key

✔ Upload encrypted data to IPFS

✔ Store the CID on a smart contract

✔ Retrieve + decrypt data locally

## This DApp is built using:

React + Vite
Ethers.js
Hardhat (Smart Contracts)
Solidity
IPFS HTTP Client
MetaMask

# steps to Run the Project
1) Check Prerequisites :- 
   1. Node.js & npm installed (Node 18 works; Node 20 is recommended) .
      
      Check:
      
          node -v
          npm -v
   3. MetaMask installed in your browser (Chrome/Brave/Edge).
   4. Open a CMD window for each component you run (you’ll need multiple terminals).
2) Start Hardhat local blockchain :-

       cd C:\path\to\your\project\hardhat
       npm install        <- run once if not already done
       npx hardhat node
    What to expect: Hardhat prints 20 accounts with private keys and addresses. Keep this
    terminal OPEN. 

     Important: Copy one of the Private Key strings (starts with 0x...). You’ll import that
     into MetaMask in a later step.

4) Deploy contracts to local Hardhat :-

    Open a new terminal

       cd C:\path\to\your\project\hardhat
       npx hardhat compile
       npx hardhat run scripts/deploy.js --network localhost
5) Run backend server

   Open a new terminal

       cd C:\path\to\your\project\backend
       npm install
       npm start
6) Prepare MetaMask (browser)
   
   https://metamask.io/download
   
   1. Click Chrome Logo
   2. Click " Add to Chrome"
   3. Then click Shortcut ( After Downlode Complete)
   4. Click a new Wallet (Login)
   5. Click Three Line -- Networks -- Add Custom network

     in this

      | Field               | Value                                          |
      | ------------------- | ---------------------------------------------- |
      | **Network Name**    | Hardhat Local                                  |
      | **RPC URL**         | [http://127.0.0.1:8545](http://127.0.0.1:8545) |
      | **Chain ID**        | 31337                                          |
      | **Currency Symbol** | ETH                                            |
          
   vi. You Are Now on Hardhat Network

      You should now see:
       Network: Hardhat Local
       Balance: $0 (but MetaMask doesn’t show local ETH)
        Don’t worry — the ETH exists.
  
6) Now IMPORT the Hardhat Account

    Go to Hardhat Node Terminal
   
    copy the PRIVATE KEY of Account #0 or any

7) Import Account in MetaMask

   In MetaMask:
     1. on left cornner click Account 1
     2. Click Add wallet -- import an account
     3. Paste Private Key of any account
     4. Click Import

8) MetaMask Now Shows 10,000 ETH

    Hardhat provides 10,000 test ETH to every default account.
    You should now see:
    10,000 ETH (not real money)
    Network: Hardhat Local
    This means your wallet is ready to sign smart contract transactions.
  
9) Start The Fronted (Vite)

       cd C:\path\to\your\project\frontend
        cd frontend
        npm install
        npm run dev
   You will see:
   
       Local: http://localhost:5173
   Open this in Chrome.

10)  Now Connect MetaMask to the site

      At the top of your frontend:
     
      Click Connect Wallet
     
      MetaMask popup opens → Click Connect
     
      Now the dApp uses your Hardhat address.

11) Click On Generate RSA Keys

12) Register Public Key On-Chain

      In the Contract field: The Contract Address is now Show in Step- 2 Terminal in coppy this
      and paste in Contract address coloumn
    
      <img width="720" height="231" alt="image" src="https://github.com/user-attachments/assets/6bacfc19-728f-422a-bc17-c00755053cc6" />

     Now click:

      Register identity (store public PEM on-chain)

14) Send Encrypted Message

    1. Enter recipient address
      (Use another imported Hardhat account)--> to Import another account  follow step- 6 and
      then step- 7
   2. Type your message: (any message)
   3. Click
       Encrypt → IPFS → Store CID on-chain

   4. Example Flow
   
    Sender (Account 1):

    Types a message

    Clicks Encrypt → IPFS → Store CID

    Gets CID: bafy123abc

    Receiver (Account 2):

    Switch MetaMask to Account 2

    Generate RSA keypair and register identity

    Paste private key in Private PEM

    Paste bafy123abc into IPFS CID

    Click Decrypt

    Message shows:
    

14) Receive & Decrypt Message

    In "Decrypt Message":

    Paste the CID that was shown under “Last CID”

    Click Decrypt

    You will now see your original message.

      Important :- you will see Last CID only when your account Key is Public or you can send
      message to your own address

     Steps or Method 1

      Go to the top of your page
      Copy your own address (the one in MetaMask).

      Paste your OWN address into
    
      Methos 2

      Put your own MetaMask address in the Recipient Address box.

    You will get your IPFS 

    If Not Get you Accunt is Private and project is !00% Done
