# Mobile Wallet Adapter Packages

This directory contains package.json files that reference the mobile wallet adapter packages from the [block-sync-one/mobile-wallet-adapter](https://github.com/block-sync-one/mobile-wallet-adapter/tree/add-sign-tx-example) repository.

## Available Packages

The following packages are available from the `add-sign-tx-example` branch:

- `@solana-mobile/mobile-wallet-adapter-protocol` - Core protocol implementation
- `@solana-mobile/mobile-wallet-adapter-protocol-web3js` - Web3.js integration
- `@solana-mobile/mobile-wallet-adapter-walletlib` - Wallet library implementation
- `@solana-mobile/wallet-adapter-mobile` - Mobile wallet adapter
- `@solana-mobile/wallet-standard-mobile` - Wallet standard for mobile

## Usage

### Option 1: Use the main package.json

Copy the `mobile-wallet-adapter-packages.json` file to your project and install dependencies:

```bash
cp mobile-wallet-adapter-packages.json your-project/
cd your-project
npm install
```

### Option 2: Add to your existing package.json

Add these dependencies to your existing `package.json`:

```json
{
  "dependencies": {
    "@solana-mobile/mobile-wallet-adapter-protocol": "github:block-sync-one/mobile-wallet-adapter#add-sign-tx-example",
    "@solana-mobile/mobile-wallet-adapter-protocol-web3js": "github:block-sync-one/mobile-wallet-adapter#add-sign-tx-example",
    "@solana-mobile/mobile-wallet-adapter-walletlib": "github:block-sync-one/mobile-wallet-adapter#add-sign-tx-example",
    "@solana-mobile/wallet-adapter-mobile": "github:block-sync-one/mobile-wallet-adapter#add-sign-tx-example",
    "@solana-mobile/wallet-standard-mobile": "github:block-sync-one/mobile-wallet-adapter#add-sign-tx-example"
  }
}
```

### Option 3: Use specific package paths

If you need to reference specific packages within the repository, use the alternative format:

```json
{
  "dependencies": {
    "@solana-mobile/mobile-wallet-adapter-protocol": "github:block-sync-one/mobile-wallet-adapter#add-sign-tx-example:js/packages/mobile-wallet-adapter-protocol",
    "@solana-mobile/wallet-adapter-mobile": "github:block-sync-one/mobile-wallet-adapter#add-sign-tx-example:js/packages/wallet-adapter-mobile"
  }
}
```

## Building the Packages

If you need to build the packages locally, you can clone the repository and build them:

```bash
git clone https://github.com/block-sync-one/mobile-wallet-adapter.git
cd mobile-wallet-adapter
git checkout add-sign-tx-example
cd js
yarn install
yarn build
```

## Notes

- These packages are from the `add-sign-tx-example` branch of the block-sync-one fork
- The packages are based on the original Solana Mobile Wallet Adapter but with modifications
- Make sure to check the specific branch for any custom changes or additions
- The packages use the same versioning as the original Solana Mobile packages

## Repository Information

- **Source**: https://github.com/block-sync-one/mobile-wallet-adapter
- **Branch**: `add-sign-tx-example`
- **Original**: Forked from solana-mobile/mobile-wallet-adapter 