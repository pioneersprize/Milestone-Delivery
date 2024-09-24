# Milestone Delivery :mailbox:


* **Application Document:** <https://github.com/pioneersprize/Polkadot-Pioneers-Prize/blob/main/applications/zklogin-Reclaim-protocol.md>
* **Milestone Number:** 1

**Context** (optional)


**Deliverables**


| Number | Deliverable | Link | Notes |
| ------------- | ------------- | ------------- |------------- |
| 1. | Integrating Reclaim Protocol with Polkadot |https://gitlab.reclaimprotocol.org/integrations/onchain/substrate-sdk (38a3b8c8e57e0bf158794fc38a0b90b73871ed61)| Use the last commit on main branch| 
| 2.  | Optimising zkProofs |https://gitlab.reclaimprotocol.org/integrations/onchain/substrate-sdk/-/blob/main/pallets/pallet-reclaim/Cargo.toml?ref_type=heads| Reclaim Polkadot SDK efficiently verifies ZKPs in the no-std environment in use (https://gitlab.reclaimprotocol.org/integrations/onchain/substrate-sdk/-/blob/main/pallets/pallet-reclaim/Cargo.toml?ref_type=heads). Verification occurs using primitive types at optimized speed—try substrate benchmarking to attest. The proofs retain cross-chain properties as cryptographic commitments are Ethereum compatible (Keccak and ECDSA) | 
| 3. | Integration and Testing | https://gitlab.reclaimprotocol.org/integrations/onchain/substrate-sdk/-/blob/main/pallets/pallet-reclaim/src/tests.rs?ref_type=heads | |
| 4. | Detailed Documentation and Guides | https://docs.reclaimprotocol.org/polkadot/substrate-quickstart | [Blog](https://questbook.notion.site/Polkadot-Blog-09e8bd01c81744bdbde912ab2a4643c8), Social Media [Announcement](https://x.com/reclaimprotocol/status/1831399357641585122?s=46) |

**Additional Information**

