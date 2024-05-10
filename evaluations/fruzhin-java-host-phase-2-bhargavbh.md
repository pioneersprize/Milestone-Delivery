# Evaluation

- **Status:** Accepted
- **Application Document:** https://github.com/pioneersprize/Polkadot-Pioneers-Prize/blob/main/applications/fruzhin-java-host-phase-2.md

- **Previously successfully merged evaluation:** Evaluation [Report](https://github.com/pioneersprize/Milestone-Delivery/blob/master/evaluations/fruzhin-java-host-phase-1-Noc2.md) of Phase-1 by Noc2

- **Milestone 1: Protocols**

| Number | Deliverable | Link | Evaluation Notes | Accepted|
| --- | --- | --- | --- | --- |
| 0. | Testing | https://github.com/LimeChain/Fruzhin/tree/dev/src/test/java/com/limechain/network/protocol | Mainly Unit test but includes some integration tests on Handshakes | <ul><li>[x] </li></ul>|
| 1. | Transactions substream | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/network/protocol/transactions | event-driven implementation for all the networking substreams  | <ul><li>[x] </li></ul> |
| 2. | Grandpa substream | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/network/protocol/grandpa | … | <ul><li>[x] </li></ul> |
| 3. | Light messages substream | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/network/protocol/lightclient | … |  <ul><li>[x] </li></ul>|
| 4. | Incoming requests for /sync/2 substream | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/network/protocol/sync | … | <ul><li>[x] </li></ul> |

- **Milestone 2: Host API**

| Number | Deliverable | Link | Notes | Accepted|
| --- | --- | --- | --- | --- |
| 0. | Testing | https://github.com/LimeChain/Fruzhin/tree/dev/src/test/java/com/limechain/runtime/hostapi | Comprehensive with mocked-up components | <ul><li>[x] </li></ul>|
| 1. | Storage API | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/runtime/hostapi/StorageHostFunctions.java | The team discussed thes on a redular basis with Spec team at W3F, all host functions implemented adhere to [Spec](https://spec.polkadot.network/chap-host-api). Both V0 and V1 storage versions are covered | <ul><li>[x] </li></ul>|
| 2. | Child Storage API | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/runtime/hostapi/ChildStorageHostFunctions.java | … | <ul><li>[x] </li></ul>|
| 3. | Crypto API | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/runtime/hostapi/CryptoHostFunctions.java | … | <ul><li>[x] </li></ul>|
| 4. | Offchain & Offchain index API | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/runtime/hostapi/OffchainHostFunctions.java | … | <ul><li>[x] </li></ul>|
| 5. | Trie API | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/runtime/hostapi/TrieHostFunctions.java | … | <ul><li>[x] </li></ul>|
| 6. | Allocator API | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/runtime/hostapi/AllocatorHostFunctions.java | … | <ul><li>[x] </li></ul>|
| 7. | Logging & Abort handler API | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/runtime/hostapi/MiscellaneousHostFunctions.java | … | <ul><li>[x] </li></ul>|

- **Milestone 3: RPC API**

| Number | Deliverable | Link | Notes | Accepted|
| --- | --- | --- | --- | --- |
| 0. | Testing | https://github.com/LimeChain/Fruzhin/tree/dev/src/test/java/com/limechain/rpc/methods | subset of the RPC endpoints compared to polkadot-sdk, nevertheless suffices for this stage of the project |<ul><li>[x] </li></ul>|
| 1. | System | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/rpc/methods/system | … |<ul><li>[x] </li></ul>|
| 2. | Chain | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/rpc/methods/chain | … |<ul><li>[x] </li></ul>|
| 3. | Offchain | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/rpc/methods/offchain | … |<ul><li>[x] </li></ul>|
| 4. | State | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/rpc/methods/state | … |<ul><li>[x] </li></ul>|
| 5. | Child State | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/rpc/methods/childstate | … |<ul><li>[x] </li></ul>|
| 6. | Sync | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/rpc/methods/sync | … |<ul><li>[x] </li></ul>|
| 7. | Add local/public and safe/unsafe RPC methods separation | https://github.com/LimeChain/Fruzhin/pull/299 | … |<ul><li>[x] </li></ul>|

- **Milestone 4: State & Sync**

| Number | Deliverable | Link | Notes | Accepted |
| --- | --- | --- | --- | --- |
| 1. | Populate state storage with official genesis state | https://github.com/LimeChain/Fruzhin/issues/213 | Supports both warp sync and full sync starting from any snapshot| <ul><li>[x] </li></ul>|
| 2. | Process genesis hashes and replace the existing hard-coded ones | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/constants/GenesisBlockHash.java | … | <ul><li>[x] </li></ul>|
| 3. | Change substream identifiers to use genesis hash | https://github.com/LimeChain/Fruzhin/pull/283 | … | <ul><li>[x] </li></ul>|
| 4. | Add child storage functionality | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/trie | … | <ul><li>[x] </li></ul>|
| 5. | Add child trie functionality | https://github.com/LimeChain/Fruzhin/tree/dev/src/main/java/com/limechain/trie	 | child trie and storage functionalities bundled in same milestone item | <ul><li>[x] </li></ul>|
| 6. | Add extrinsics validation | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/sync/fullsync/FullSyncMachine.java#L107 | | <ul><li>[x] </li></ul>|
| 7. | Add configuration to start full node using either warp or full sync | https://github.com/LimeChain/Fruzhin/blob/dev/src/main/java/com/limechain/sync/SyncMode.java | … | <ul><li>[x] </li></ul>|


- **Milestone 5: Modularisation**

| Number | Deliverable | Link | Notes | Accepted|
| --- | --- | --- | --- | --- |
| 1. | Code base improvements | https://github.com/LimeChain/Fruzhin/pull/338 | Codebase is reasonably modular |<ul><li>[x] </li></ul>|



- **Milestone 6: VRF Proofs**

| Number | Deliverable | Link | Notes | Accepted|
| --- | --- | --- | --- | --- |
| 1. | DLEQ Proofs Generation | https://github.com/LimeChain/polkaj/pull/2 | Not an expert in VRFs, the transcripts seem to match the spec | <ul><li>[x] </li></ul>|
| 2. | DLEQ Proofs Verification | https://github.com/LimeChain/polkaj/pull/2 | … | <ul><li>[x] </li></ul>|


- **Milestone 7: Light Client & Full Node Support**

| Number | Deliverable | Link | Notes | Accepted
| --- | --- | --- | --- | --- |
| 1. | Light client issues support | We haven’t received user feedback, but we refactor a couple of small things improving the warp sync speed. | milestone's objective is unclear as fruzhin is not in use. Limechain should probably carry over the support as part of phase-3 hopefully with a non-negligible user base |  <ul><li>[] </li></ul>|
| 2. | Full node issues support | Fixed a couple of small issues and added optional checks such as the check_inherents call before every “Core_execute_block” call. | milestone's objective is unclear as fruzhin is not in use. Limechain should probably carry over the support as part of phase-3 hopefully with a non-negligible usercbase  | <ul><li>[] </li></ul>|

- **Milestone 8: Zombienet tests**

| Number | Deliverable | Link | Notes | Accepted|
| --- | --- | --- | --- | --- | 
| 1. | Add test to showcase successful block building(full node) | https://github.com/LimeChain/Fruzhin/blob/dev/zombienet/0003-block-execution.toml | tests in simulation network |  <ul><li>[x] </li></ul>|
| 2. | Add test to showcase successful block header verification(light client) | https://github.com/LimeChain/Fruzhin/blob/dev/zombienet/0001-light-client-header-verification.toml | … | <ul><li>[x] </li></ul>|
| 3. | Add test to showcase successful peer finding | https://github.com/LimeChain/Fruzhin/blob/dev/zombienet/0002-peer-discovery.toml | ... | <ul><li>[x] </li></ul>|



- **Milestone 9: Repository Maintenance**

| Number | Deliverable | Link | Notes | Accepted |
| --- | --- | --- | --- | --- |
| 1. | Create a code of conduct. | https://github.com/LimeChain/Fruzhin/pull/321 | Best Practices have been followed for CI and workflow automation |  <ul><li>[x] </li></ul>|
| 2. | Add License | https://github.com/LimeChain/Fruzhin?tab=Apache-2.0-1-ov-file | … | <ul><li>[x] </li></ul>|
| 3. | Add Contributor guidelines that outline the steps for contributors | https://github.com/LimeChain/Fruzhin/pull/321 |  | <ul><li>[x] </li></ul>|
| 4. | Issues and pull request templates | https://github.com/LimeChain/Fruzhin/pull/321 |  | <ul><li>[x] </li></ul>|
| 5. | Changelog | https://github.com/LimeChain/Fruzhin/blob/dev/.github/workflows/release.yml#L34 |  | <ul><li>[x] </li></ul>|
| 6. | Dependabot setup | https://github.com/LimeChain/Fruzhin/pull/321 |  | <ul><li>[x] </li></ul>|
| 7. | Binary | https://github.com/LimeChain/Fruzhin/pull/321 |  | <ul><li>[x] </li></ul>|


- **Milestone 10: Documentation & Guides**

| Number | Deliverable | Link | Notes | Accepted |
| --- | --- | --- | --- | --- |
| 0. | Article | https://limechain.tech/blog/fruzhin-empowering-polkadot-client-development/ | Documentation in core codebase is sparser than ideal  |  <ul><li>[x] </li></ul>|
| 1. | Documentation | No link possible as the documentation is not only in 1 place. We made readme improvements and we added a lot of inline documentation. | … |  <ul><li>[x] </li></ul>|


- **Milestone 11: Research**

| Number | Deliverable | Link | Notes | Accepted |
| --- | --- | --- | --- | --- |
| 1. | Research | We researched different ways to improve the trie structure as it was the one causing us the most trouble. We have scoped a plan for making it work faster but it would require a bit more time so we will do it in the next phase. | W3F is aware of the ambiguities in trie spec and all the corner cases that have to be dealt with. We definitely would like to see you experience documented. Suggest transferring this milestone concretely as part Phase-3 |  <ul><li>[x] </li></ul>|


- **Milestone 12: Developer Relations**

| Number | Deliverable | Link | Notes | Accepted |
| --- | --- | --- | --- | --- |
| 1. | Establish a community channel for support, questions and feedback | https://discord.gg/sSkWWHNm | … |
| 2. | Create a demo showcasing the full node | https://youtu.be/-Q0Be5coP-A |



## Overall Evaluation

The team has done a great job in developing  a full node, supporting both warp and full sync. Initial concerns raised on the client unable to fetch and load the runtime have been fixed. Another issue on sync abruptly ending on westend  also has been fixed. One issue still persists that the node gets stuck stuck at the last-but-one epoch when warp syncing, which is proposed to be resolved in Phase-3-Milestone-4-Task-8. I suggest concretely adding this as a Milestone. 
I also suggest transferring Milestone-7 (Light Client & Full Node Support) to Phase-3 as these are not relevant without any user-base.
Similarly, Milestone-11 (research on trie structure) can be transferred to Phase-3.
Fruzhin feature-wise is in a state where it can be used as a light client. We encourage you to have a strong outreach campaign to spread the word and attract users. We can put you in touch with W3F communications team for any support. 
