# Poly-Bridge

# Final Challenge Project - NFT Collection

## Overview

This project involves creating a 5-item NFT collection using AI image generation tools (DALLE 2 or Midjourney), storing these items on IPFS using Pinata, and deploying an ERC721 or ERC1155 contract on the sepolia Ethereum Testnet. The project also includes mapping the NFT collection on the Polygon network, batch minting the NFTs, and transferring them to Polygon amoy using the FxPortal Bridge.

## Project Requirements

### Generate NFT Collection

1. **Generate Images:**
   - Use DALLE 2 or Midjourney to generate a 5-item collection.
   - Save the prompt used for generating each image.

2. **Store on IPFS:**
   - Store the generated images on IPFS using [pinata.cloud](https://pinata.cloud/).

### Smart Contract Deployment

3. **Deploy Contract:**
   - Deploy an ERC721 or ERC1155 contract on the sepolia Ethereum Testnet.
   - Include a `promptDescription` function that returns the prompt used to generate the images.

4. **Map NFT Collection:**
   - (Optional) Map your NFT collection using the Polygon network token mapper for better visualization.

### Hardhat Scripts

5. **Batch Mint NFTs:**
   - Write a Hardhat script to batch mint all NFTs. Using ERC721A is recommended for this task.

6. **Batch Transfer NFTs:**
   - Write a Hardhat script to batch transfer all NFTs from Ethereum to Polygon amoy using the FxPortal Bridge.

### Approve and Transfer NFTs

7. **Approve NFTs:**
   - Approve the NFTs to be transferred.

8. **Deposit NFTs:**
   - Deposit the NFTs to the Bridge.

### Test

9. **Test Balance:**
   - Verify the balance of the NFTs on the amoy network.

## Installation

1. Clone the repository:
    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2. Install dependencies:
    ```bash
    npm install
    ```

3. Set up environment variables by creating a `.env` file in the root directory with the following:
    ```bash
    sepolia_RPC_URL=<Your sepolia RPC URL>
    POLYGON_amoy_RPC_URL=<Your Polygon amoy RPC URL>
    PRIVATE_KEY=<Your Private Key>
    PINATA_API_KEY=<Your Pinata API Key>
    PINATA_SECRET_API_KEY=<Your Pinata Secret API Key>
    ```

## Usage

### Deploy Contract

1. Compile the contracts:
    ```bash
    npx hardhat compile
    ```

2. Deploy the contract:
    ```bash
    npx hardhat run scripts/deploy.js 
    ```

### Mint NFTs

1. Batch mint NFTs:
    ```bash
    npx hardhat run scripts/batchMint.js 
    ```

### Transfer NFTs

1. Approve NFTs for transfer:
    ```bash
    npx hardhat run scripts/approveNFTs.js 
    ```

2. Deposit NFTs to the Bridge:
    ```bash
    npx hardhat run scripts/depositNFTs.js 
    ```

3. Test balance on amoy:
    ```bash
    npx hardhat run scripts/testBalance.js 
    ```

## Scripts

- `deploy.js`: Deploys the NFT contract to the sepolia Testnet.
- `batchMint.js`: Batch mints all NFTs.
- `approveNFTs.js`: Approves the NFTs for transfer.
- `depositNFTs.js`: Deposits the NFTs to the FxPortal Bridge.
- `testBalance.js`: Checks the balance of NFTs on the amoy network.

## Additional Resources

- [Hardhat Documentation](https://hardhat.org/getting-started/)
- [Pinata Cloud](https://pinata.cloud/documentation)
- [ERC721A Documentation](https://github.com/chiru-labs/ERC721A)
- [FxPortal Bridge](https://docs.polygon.technology/docs/develop/l1-l2-communication/fx-portal/)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Special thanks to the creators of Hardhat and Foundry for providing powerful development tools.
- Thanks to Pinata for providing easy-to-use IPFS pinning services.
- Gratitude to the Polygon team for their extensive documentation and support.

---

Feel free to reach out if you have any questions or need further assistance. Happy coding!
