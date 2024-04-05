# Drops SOL
Drops is an SOLANA, token-integrated locked liquidity marketplace, allowing;
- Holders to stabilize token price via staking and liquidity provision in return for a share of total platform revenues.
- Marketplace users to actively trade locked liquidity, a once illiquid asset.

## Description
Unlock the power of DROPS, your ultimate platform for seamlessly buying, selling, and trading Solana-locked liquidity. Experience the freedom of our peer-to-peer decentralized marketplace, where liquidity flows effortlessly. Alternatively, utilize SOL to access our premium services for a nominal fee. Join us and elevate your trading experience with DROPS today.

## Features
- List LP token locks for sale on Solana.
- Purchase LP token locks with SOL or Drops tokens.
- Secure and non-reentrant contract design.

## Contract Methods
- `setDropsToken`: Set the address of the Drops token.
- `setFeeWallet`: Set the address of the fee wallet.
- `setLockerAddress`: Set the address of the locker contract (Raydium).
- `initiateListing`: List an LP token lock for sale.
- `activateListing`: Activate an initiated listing.
- `buyLockWithSOL`: Purchase a listed LP token lock with SOL.
- `buyLockWithDrops`: Purchase a listed LP token lock with Drops tokens.
- `withdrawListing`: Withdraw a listed LP token lock.
- `changePriceInSOL`: Change the SOL price of a listing.
- `changePriceInDrops`: Change the Drops token price of a listing.

## Contributing
No contributions will be accepted.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

