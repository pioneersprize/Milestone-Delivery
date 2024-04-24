# Fruzhin Java Host Phase 2 Milestone Delivery

- **Application Document:** https://github.com/pioneersprize/Polkadot-Pioneers-Prize/blob/main/applications/fruzhin-java-host-phase-2.md

<br/><br/>
- **Milestone Number:** 1
- **Context:** Protocols

**Deliverables:**

| Number | Deliverable | Link | Notes |
| --- | --- | --- | --- |
| 0. | Testing | https://github.com/LimeChain/Fruzhin/tree/dev/src/test/java/com/limechain/network/protocol |  |
| 1. | Transactions substream | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/network/protocol/transactions | … |
| 2. | Grandpa substream | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/network/protocol/grandpa | … |
| 3. | Light messages substream | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/network/protocol/lightclient | … |
| 4. | Incoming requests for /sync/2 substream | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/network/protocol/sync | … |

<br/><br/>
- **Milestone Number:** 2
- **Context:**: Host API

**Deliverables:**

| Number | Deliverable | Link | Notes |
| --- | --- | --- | --- |
| 0. | Testing | https://github.com/LimeChain/Fruzhin/tree/dev/src/test/java/com/limechain/runtime/hostapi |  |
| 1. | Storage API | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/runtime/hostapi/StorageHostFunctions.java | … |
| 2. | Child Storage API | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/runtime/hostapi/ChildStorageHostFunctions.java | … |
| 3. | Crypto API | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/runtime/hostapi/CryptoHostFunctions.java | … |
| 4. | Offchain & Offchain index API | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/runtime/hostapi/OffchainHostFunctions.java | … |
| 5. | Trie API | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/runtime/hostapi/TrieHostFunctions.java | … |
| 6. | Allocator API | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/runtime/hostapi/AllocatorHostFunctions.java | … |
| 7. | Logging & Abort handler API | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/runtime/hostapi/MiscellaneousHostFunctions.java | … |

<br/><br/>
- **Milestone Number:** 3
- **Context:** RPC API

**Deliverables:**

| Number | Deliverable | Link | Notes |
| --- | --- | --- | --- |
| 0. | Testing | https://github.com/LimeChain/Fruzhin/tree/dev/src/test/java/com/limechain/rpc/methods |  |
| 1. | System | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/rpc/methods/system | … |
| 2. | Chain | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/rpc/methods/chain | … |
| 3. | Offchain | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/rpc/methods/offchain | … |
| 4. | State | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/rpc/methods/state | … |
| 5. | Child State | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/rpc/methods/childstate | … |
| 6. | Sync | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/rpc/methods/sync | … |
| 7. | Add local/public and safe/unsafe RPC methods separation | https://github.com/LimeChain/Fruzhin/pull/299 | … |

<br/><br/>
- **Milestone Number:** 4
- **Context:** State & Sync
  
**Deliverables:**

| Number | Deliverable | Link | Notes |
| --- | --- | --- | --- |
| 1. | Populate state storage with official genesis state | https://github.com/LimeChain/Fruzhin/issues/213 | … |
| 2. | Process genesis hashes and replace the existing hard-coded ones | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/constants/GenesisBlockHash.java | … |
| 3. | Change substream identifiers to use genesis hash | https://github.com/LimeChain/Fruzhin/pull/283 | … |
| 4. | Add child storage functionality | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/trie | … |
| 5. | Add child trie functionality | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/trie	 | We bundled the child trie and storage functionalities in the above milestone item |
| 6. | Add extrinsics validation | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/sync/fullsync/FullSyncMachine.java#L107 | check_inherents call followed by a Core_execute_block |
| 7. | Add configuration to start full node using either warp or full sync | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/sync/SyncMode.java | … |

<br/><br/>
- **Milestone Number:** 5
- **Context**: Modularisation

**Deliverables:**

| Number | Deliverable | Link | Notes |
| --- | --- | --- | --- |
| 1. | Code base improvements | https://github.com/LimeChain/Fruzhin/pull/338 | … |

<br/><br/>
- **Milestone Number:** 6
- **Context:** VRF Proofs

**Deliverables**

| Number | Deliverable | Link | Notes |
| --- | --- | --- | --- |
| 1. | DLEQ Proofs Generation | https://github.com/LimeChain/polkaj/pull/2 | … |
| 2. | DLEQ Proofs Verification | https://github.com/LimeChain/polkaj/pull/2 | … |

<br/><br/>
- **Milestone Number:** 7
- **Context:** Light Client & Full Node Support

**Deliverables:**

| Number | Deliverable | Link | Notes |
| --- | --- | --- | --- |
| 1. | Light client issues support | We haven’t received user feedback, but we refactor a couple of small things improving the warp sync speed. | … |
| 2. | Full node issues support | Fixed a couple of small issues and added optional checks such as the check_inherents call before every “Core_execute_block” call. | … |

<br/><br/>
- **Milestone Number:** 8
- **Context:** Zombienet tests

**Deliverables:**

| Number | Deliverable | Link | Notes |
| --- | --- | --- | --- |
| 1. | Add test to showcase successful block building(full node) | https://github.com/LimeChain/Fruzhin/blob/dev/zombienet/0003-block-execution.toml | … |
| 2. | Add test to showcase successful block header verification(light client) | https://github.com/LimeChain/Fruzhin/blob/dev/zombienet/0001-light-client-header-verification.toml | … |
| 3. | Add test to showcase successful peer finding | https://github.com/LimeChain/Fruzhin/blob/dev/zombienet/0002-peer-discovery.toml |  |

<br/><br/>
- **Milestone Number:** 9
- **Context:** Repository Maintenance

**Deliverables:**

| Number | Deliverable | Link | Notes |
| --- | --- | --- | --- |
| 1. | Create a code of conduct. | https://github.com/LimeChain/Fruzhin/pull/321 | … |
| 2. | Add License | https://github.com/LimeChain/Fruzhin?tab=Apache-2.0-1-ov-file | … |
| 3. | Add Contributor guidelines that outline the steps for contributors | https://github.com/LimeChain/Fruzhin/pull/321 |  |
| 4. | Issues and pull request templates | https://github.com/LimeChain/Fruzhin/pull/321 |  |
| 5. | Changelog | https://github.com/LimeChain/Fruzhin/blob/dev/.github/workflows/release.yml#L34 |  |
| 6. | Dependabot setup | https://github.com/LimeChain/Fruzhin/pull/321 |  |
| 7. | Binary | https://github.com/LimeChain/Fruzhin/pull/321 |  |

<br/><br/>
- **Milestone Number:** 10
- **Context:** Documentation & Guides

**Deliverables:**

| Number | Deliverable | Link | Notes |
| --- | --- | --- | --- |
| 0. | Article | https://limechain.tech/blog/fruzhin-empowering-polkadot-client-development/ | … |
| 1. | Documentation | No link possible as the documentation is not only in 1 place. We made readme improvements and we added a lot of inline documentation. | … |

<br/><br/>
- **Milestone Number:** 11
- **Context:** Research

**Deliverables:**

| Number | Deliverable | Link | Notes |
| --- | --- | --- | --- |
| 1. | Research | We researched different ways to improve the trie structure as it was the one causing us the most trouble. We have scoped a plan for making it work faster but it would require a bit more time so we will do it in the next phase. | … |


- **Milestone Number:** 12
- **Context:** Developer Relations

> The milestone items listed here don’t correlate 1 to 1 with the ones in the proposal.  We have spoken with people from the foundation about small changes to this milestone.

**Deliverables**

| Number | Deliverable | Link | Notes |
| --- | --- | --- | --- |
| 1. | Establish a community channel for support, questions and feedback | https://discord.gg/sSkWWHNm | … |
| 2. | Create a demo showcasing the full node | https://youtu.be/-Q0Be5coP-A |
