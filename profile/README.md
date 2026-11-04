# ipsa

ibc v2 for stellar. each chain verifies the other's consensus in on-chain code, with no bridge operator, custodian or attestation service in the trust path.

- **website** - [ipsa.dev](https://ipsa.dev)
- **app** - [app.ipsa.dev](https://app.ipsa.dev): docs, the scp verifier, the explorer and transfers

## how it works

- **stellar side** - soroban contracts implement ibc v2, so stellar sends and receives packets as a first-class member of the protocol.
- **counterparty side** - a stellar light client checks stellar's scp signatures against a trust root of validators. the cosmos hub runs it as an 08-wasm client, and ethereum checks it through sp1 zero-knowledge proofs.
- **relayer** - carries the bytes and has no authority. if it lies, the proofs fail. if it stops, packets time out and funds return to the sender.

corridors live on testnet today: stellar ↔ cosmos hub, and stellar ↔ sepolia.

## repositories

- [stellar-light-client](https://github.com/ipsadev/stellar-light-client) - the 08-wasm stellar light client for cosmwasm chains
- [ibc-contracts](https://github.com/ipsadev/ibc-contracts) - ibc v2 solidity contracts with the stellar corridor, the sp1 programs and the proof api
- [stellar-consensus-verifier](https://github.com/ipsadev/stellar-consensus-verifier) - scp verification in rust
- [ipsa-scp-verifier](https://github.com/ipsadev/ipsa-scp-verifier) - verify one ledger's consensus, step by step, from the history archives
- [ipsa-ibc-core](https://github.com/ipsadev/ipsa-ibc-core) - ibc commitment paths, the fixed-depth smt and its ics-23 proofs
- [ibc-relayer](https://github.com/ipsadev/ibc-relayer) - cosmos labs' ibc v2 relayer with stellar as a chain type, under their source-available evaluation licence

the rest of the implementation is private while it is under active development, and will be open-sourced once it stabilises.
