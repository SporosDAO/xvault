# xVault

Multi-chain DAO vault that provides a deterministic address on ETH L1 and EVM equivalent L2s (Arbitrum One, Optimism, etc.). Allows DAOs to deploy xVault across multipl chains with the exact same deployment address. Consequently DAOs can receive funds on the same xVault address across multiple chains and control the funds in each vault from their main Kali smart contract deployment on an ETH L1 or EVM-equivalent L2 chain.

It provides DAOs with direct control of their assets using a single convenient address, similar to Extenally Owned Accounts created via in MetaMask or Ledger wallets, but without the liability associated with individual and multisig custodians of DAO assets.

# User Stories:

1. Receiving Gitcoin awards in a DAO vault instead of a personal externally owned address or a multi-sig.
  - Receving funds in a personal EOA triggers income tax event for the recipient. The person has to deduct income tax before forwarding the funds to the DAO that they are inteded for. After forwarding the funds to the DAO , that may trigger another tax event for the DAO itself.
  - Receiving funds in non-multi-chain contract address such as a Gnosis-safe leads to lost funds. If the Gnosis Safe is deployed on L1, and donors send funds to L2s (zkSync, Arbitrum One, Polygon), then the funds on L2s are lost unless the Gnosis-safe safe has been deployed on the exact same address on all L2s. As of July 2022, it is not straightforward to deploy a Gnosis safe on multiple chains with the same address.
  - Receiving funds in a DAO's main contract address also leads to lost funds. If the DAO contract is deployed on Arbitrbum One and donors send funds to L1 or another L2, there is no way for the DAO to control these funds.
2. Real world [Sporos DAO example](https://gitcoin.co/grants/6035/sweat-equity-management-platform-for-daos) with gitcoin funding.
    - Funds from the example above were sent to the correct DAO address `0x28feac06dc72188b385478b507f7c7a39a7026d5` but not on the DAO native chain where the [DAO smart contract was deployed (Arbitrum One)](0x28feac06dc72188b385478b507f7c7a39a7026d5). Instead funds were sent to L1, zkSync and Polygon. None of the funds can be accessed by the DAO now.
2. [LexDAO discussion](https://discord.com/channels/682960432272506907/900411400491524106/998084170666475520) on shuffling funds from multi-sigs to DAO governed contracts on multiple chains.

2. [Optimism to Wintermute transaction lost 20M](https://cryptobriefing.com/wintermute-makes-optimistic-assumption-loses-20m-optimism-tokens/).

# Design

Working draft of [xVault design doc here](https://github.com/SporosDAO/sweat-token/wiki/xVault:-Multi-chain-DAO-Treasury-Vault).
