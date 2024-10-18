# ENS dApp

This project is a decentralized application (dApp) built using the ENS (Ethereum Name Service) to display and interact with ENS names associated with wallet addresses. It connects to the Ethereum Sepolia testnet and allows users to view their ENS names (if available) or their wallet addresses if they do not have an ENS name. The dApp is integrated with **RainbowKit** to handle wallet connections and **Wagmi** to manage Ethereum interactions.

## Features

- **Wallet Connection**: Users can connect their wallets via RainbowKit using multiple wallet options such as MetaMask, Ledger, TrustWallet, and Argent.
- **ENS Name Display**: If a user has an ENS name associated with their connected wallet, the dApp displays their ENS name. If no ENS name exists, the wallet address is shown instead.
- **Ethereum Sepolia Testnet**: The dApp runs on the Sepolia testnet.
- **React Query Integration**: The app uses **TanStack Query** (React Query) for efficient data fetching, caching, and synchronization with external APIs.

## Technologies Used

- **Next.js**: Framework for building the user interface.
- **RainbowKit**: Library for easy wallet integration.
- **Wagmi**: Ethereum hooks for React to interact with Ethereum wallets and chains.
- **React Query**: For handling data fetching and caching.
- **TailwindCSS**: For styling the UI components.
- **Sepolia Testnet**: Ethereum test network for development.

## Project Structure

```
📦ens-dapp
 ┣ 📂components
 ┣ 📂public
 ┣ 📂styles
 ┣ 📜globals.css
 ┣ 📜index.js
 ┣ 📜layout.js
 ┣ 📜providers.js
 ┣ 📜README.md
```

### Key Files

- **RootLayout**: Defines the base layout of the dApp and includes the `Providers` component for context.
- **Providers.js**: Provides the Wagmi, RainbowKit, and React Query configurations.
- **Home.js**: Contains the logic for rendering the main page of the dApp, connecting to wallets, and displaying ENS names or wallet addresses.

## Setup and Installation

### Requirements

- Node.js (v14 or higher)
- Yarn or npm

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/ens-dapp.git
   ```

2. Navigate into the project directory:

   ```bash
   cd ens-dapp
   ```

3. Install the required dependencies:

   ```bash
   npm install
   ```

   or

   ```bash
   yarn install
   ```

4. Create a `.env` file at the root of the project and add the following:

   ```bash
   PROJECT_ID=your-infura-or-rainbowkit-project-id
   ```

5. Start the development server:

   ```bash
   npm run dev
   ```

   or

   ```bash
   yarn dev
   ```

6. Open the app in your browser at `http://localhost:3000`.

## Environment Variables

The app requires the following environment variable to be set in the `.env` file:

- **PROJECT_ID**: The Project ID from either Infura or RainbowKit for connecting to the Ethereum network.

## How It Works

1. **Wallet Connection**: Users can connect their Ethereum wallets via the RainbowKit `ConnectButton`. Once connected, their wallet address or ENS name will be displayed.
2. **ENS Name Resolution**: The dApp fetches the ENS name of the connected wallet using the `useEnsName` hook from the Wagmi library.
3. **Sepolia Chain**: The app is configured to run on the Sepolia Ethereum testnet, ensuring that it's running in a test environment for developers.

## Future Enhancements

- Add more wallet options.
- Support for other Ethereum chains (e.g., mainnet, Goerli).
- Implement additional ENS features such as ENS registration.
- Improve error handling and user feedback.

## Acknowledgements

This project is inspired by the **LearnWeb3 Punks** NFT collection and dApp tutorials. It uses various open-source tools and libraries such as RainbowKit, Wagmi, and React Query to simplify wallet and Ethereum interaction for developers.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any inquiries or contributions, please feel free to reach out.
