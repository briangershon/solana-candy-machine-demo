# solana-candy-machine-demo

From https://docs.metaplex.com/candy-machine-v2/introduction

## Setup

Get environment setup for devnet development:

https://docs.metaplex.com/candy-machine-v2/getting-started

## Deploy Candy Machine

Grab you local wallet address vs `solana address`.

Update `config.json` `solTreasuryAccount` with that wallet address.

Deploy:

```
npx ts-node ~/metaplex/js/packages/cli/src/candy-machine-v2-cli.ts upload \
    -e devnet \
    -k ~/.config/solana/devnet.json \
    -cp config.json \
    -c example \
    ./assets
```

Check deploy explorer.solana.com:

Visit <https://explorer.solana.com/?cluster=devnet>

Verify uploads:

```
npx ts-node ~/metaplex/js/packages/cli/src/candy-machine-v2-cli.ts verify_upload \
    -e devnet \
    -k ~/.config/solana/devnet.json \
    -c example
```

Mint one token:

```
npx ts-node ~/metaplex/js/packages/cli/src/candy-machine-v2-cli.ts mint_one_token \
    -e devnet \
    -k ~/.config/solana/devnet.json \
    -c example
```
