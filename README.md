# Lottery Smart Contract README

## Overview
This repository contains the code for a decentralized lottery smart contract deployed on a blockchain testnet. The smart contract is implemented in Solidity and was initially developed using Remix IDE. The front end is a simple HTML page hosted on GitHub Pages, interacting with the smart contract through the Web3.js library.

## Smart Contract (Lotteryv0.sol)
### Contract Details
- **Contract Name:** Lotteryv0
- **Manager:** The manager is the address that deployed the contract and has special privileges.
- **Participants:** An array of payable addresses representing participants in the lottery.

### Functions
- **Constructor:**
  - Initializes the manager with the address of the contract deployer.

- **Enter:**
  - Allows users to enter the lottery by sending a minimum of 0.01 ETH.
  - Usage: `enter()`

- **Random:**
  - Private function to generate a pseudo-random number based on block information and participant addresses.
  - Usage: `random()`

- **Pick Winner:**
  - Only the manager can trigger this function.
  - Randomly selects a participant and transfers the contract balance to their address.
  - Resets the participants array for the next round.
  - Usage: `pickWinner()`

- **Get Participants:**
  - Returns the array of participant addresses.
  - Usage: `getParticipants()`

### Modifiers
- **Restricted:**
  - Ensures that only the manager can execute certain functions.

## Front End (index.html)
### Technologies Used
- HTML
- Web3.js (v1.3.0)

### Connecting to the Smart Contract
- **Connect to Wallet:**
  - Click the "Connect to Wallet" button to connect your MetaMask wallet.

- **Enter Lottery:**
  - After connecting, use the "Enter" button to participate in the lottery by sending 0.01 ETH.

- **Pick Winner:**
  - If you are the manager, use the "Pick Winner" button to randomly select a winner.

- **Display Participants:**
  - The "Participants" section displays the list of current participants.

## HOW TO USE
Follow these step-by-step instructions to interact with the lottery smart contract:

1. **Deploy Smart Contract on Remix IDE**
   - Open Remix IDE (https://remix.ethereum.org/).
   - Copy and paste the content of `Lotteryv0.sol` into the editor.
   - Compile and deploy the contract on a blockchain testnet (e.g., Rinkeby).

2. **Host Front End on GitHub Pages**
   - Fork this repository on GitHub.
   - Navigate to the "Settings" tab of your forked repository.
   - Scroll down to the "GitHub Pages" section and choose the `index.html` file as the source.
   - Update the `contractAddress` variable in the HTML file with the deployed smart contract address.

3. **Access the Lottery Application**
   - Open the hosted HTML page on GitHub Pages.

4. **Connect MetaMask Wallet**
   - Click the "Connect to Wallet" button.
   - If using MetaMask, approve the connection.

5. **Enter the Lottery**
   - Click the "Enter" button to participate by sending 0.01 ETH.

6. **Pick a Winner (Manager Only)**
   - If you are the manager, click the "Pick Winner" button to randomly select a winner.

7. **Display Participants**
   - The "Participants" section displays the list of current participants.

## Important Notes
- Ensure MetaMask is installed and configured.
- The manager is the only entity authorized to pick a winner.
- A minimum of 3 participants is required for a valid winner selection.

Feel free to explore and enhance the functionality of this lottery smart contract. If you encounter any issues, refer to the provided documentation or contact the developer. Happy lotterying!
