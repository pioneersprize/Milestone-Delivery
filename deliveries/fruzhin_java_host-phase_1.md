# Fruzhin Java Host Phase 1 Milestone Delivery

- **Application Document:** https://github.com/pioneersprize/Polkadot-Pioneers-Prize/blob/main/applications/fruzhin-java-host-phase-1.md
- **Milestone Number:** all

**Context** (optional)

The Milestones here make for a complete light client capable of discovering other nodes, exchanging handshakes with them, performing warp sync + full sync and handling rpc requests.

**Deliverables**

| Number | Deliverable | Link | Notes |
| --- | --- | --- | --- |
| 1a. | Repository setup | https://github.com/LimeChain/Fruzhin | … |
| 1b. | Chain specification | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/chain/ChainSpec.java | … |
| 1c. | RocksDB setup | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/storage/DBInitializer.java | … |
| 1d. | Fork & Improve PolkaJ’s SCALE | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/sync/warpsync/scale | https://github.com/limechain/polkaj |
| 1e. | Setup RPC module | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/rpc/methods/RPCMethodsImpl.java | … |
| 1f. | Forward light-client-specific endpoints | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/rpc/server/RpcWsHandler.java | … |
| 1g. | CLI + CI/CD setup | https://github.com/LimeChain/Fruzhin/actions/workflows/gradle.yml | … |
| 1h. | Unit tests | https://github.com/LimeChain/Fruzhin/tree/dev/src/test/java/com/limechain | Linking to the general tests directory as there are too many files to list here |
| 2a. | Modify Nabu’s strict spec Kademlia implementation in order to conform to the libp2p specification | https://github.com/LimeChain/nabu/blob/master/src/main/java/org/peergos/protocol/dht/Kademlia.java | … |
| 2b. | Create a network module which will hold P2P business logic | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/network/Network.java | … |
| 2c. | Forward RPC requests after peers are found | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/rpc/subscriptions/chainhead/ChainHeadRpcImpl.java | … |
| 2d. | Extend the system RPC module with data coming from the P2P connection and implement methods that provide peer information | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/rpc/methods/system/SystemRPCImpl.java | … |
| 2e. | Unit tests | https://github.com/LimeChain/Fruzhin/blob/dev/src/test/java/com/limechain/network/kad/KademliaServiceTest.java | … |
| 3a. | Add substream negotiation logic | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/network/protocol/warp/WarpSync.java | … |
| 3b. | Integrate Yamux substreams into the light client logic | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/network/Network.java#L90 | … |
| 3c. | Unit tests | https://github.com/LimeChain/Fruzhin/tree/dev/src/test/java/com/limechain/network/protocol | … |
| 4a. | Patch and update wasmer-java | https://github.com/LimeChain/wasmer-java/blob/dev/src/java/org/wasmer/ImportObject.java#L73 | Link points to the added MemoryImport static class because that was one of bigger changes that needed to be made in the repo, the other changes are too small to warrant a link. |
| 4b. | Create Host module | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/runtime/hostapi/HostApi.java | … |
| 4c. | Create runtime module | https://github.com/LimeChain/Fruzhin/commit/633397721b7650c0919556ece3c3c7f49c9ab4de#diff-71216f7097ee576856d8481dabe8cfd48ba44259ae759e6692148fa9f5df3e26R194 | The reason this is the only milestone linked with a commit hash is because it’s the only functionality that’s not merged yet. |
| 4d. | Unit tests | https://github.com/LimeChain/wasmer-java/tree/dev/test/org/wasmer | … |
| 5. | Documentation | - | Inline documentation can be found within the classes. |

**Additional Information**
