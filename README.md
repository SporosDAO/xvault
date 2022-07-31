# xVault

Multi-chain DAO vault that has the same address on L1 and L2s.

# User Stories:

1. Receiving gitcoin awards in a DAO vault instead of a personal address.
  - Receving funds in a personal EOA triggers income tax event for the recipient. The person has to deduct income tax before forwarding the funds to the DAO that they are inteded for. After forwarding the funds to the DAO , that may trigger another tax event for the DAO itself.
  - Receiving funds in non-multi-chain contract address such as a Gnosis-safe leads to lost funds. If the Gnosis Safe is deployed on L1, and donors send funds to L2s (zkSync, Arbitrum One, Polygon), then the funds on L2s are lost unless the Gnosis-safe safe has been deployed on the exact same address on all L2s. As of July 2022, it is not straightforward to deploy a Gnosis safe on multiple chains with the same address.
  - Receiving funds in a DAO's main contract address also leads to lost funds. If the DAO contract is deployed on Arbitrbum One and donors send funds to L1 or another L2, there is no way for the DAO to control these funds.
  - Real world example: https://gitcoin.co/grants/6035/sweat-equity-management-platform-for-daos
  - Funds from the example above we sent to the DAO address but on L1, zkSync and Polygon. None of the funds can be used by the DAO contract which was deployed on Arbitrum One.



# Design

Draft design doc here.
