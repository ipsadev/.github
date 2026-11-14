# ipsa

light clients for ibc v2. each chain verifies the other's consensus in on-chain code, with no bridge operator, custodian or attestation service in the trust path. stellar is the first chain; corridors to cosmos hub and sepolia are live on testnet.

[ipsa.dev](https://ipsa.dev) · [app](https://app.ipsa.dev) · [technical documentation](https://app.ipsa.dev/docs)

## repositories

- [ipsa-contracts](https://github.com/ipsadev/ipsa-contracts) - ibc v2 as soroban contracts on stellar
- [stellar-light-client](https://github.com/ipsadev/stellar-light-client) - the 08-wasm stellar light client for cosmos chains
- [ibc-contracts](https://github.com/ipsadev/ibc-contracts) - ibc v2 solidity contracts with the stellar corridor and its sp1 proofs
- [stellar-consensus-verifier](https://github.com/ipsadev/stellar-consensus-verifier) - scp verification in rust
- [ipsa](https://github.com/ipsadev/ipsa) - the ipsa crate and example apps
- [ipsa-gateway](https://github.com/ipsadev/ipsa-gateway) - grpc gateway for ipsa
- [ibc-relayer](https://github.com/ipsadev/ibc-relayer) - cosmos labs' ibc v2 relayer with stellar as a chain type, under their source-available evaluation licence

the backend, cli and apps are private for now.
