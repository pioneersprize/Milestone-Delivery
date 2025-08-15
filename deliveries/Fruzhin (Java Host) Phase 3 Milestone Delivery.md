# Fruzhin Java Host Phase 3 Milestone Delivery

**Application Document:** 
Please refer to the [Phase 3 Proposal](https://github.com/pioneersprize/Polkadot-Pioneers-Prize/pull/15/files?short_path=1954df8#diff-1954df878dbf6b2e5333bb29c366bfb696d9bb8b0fbbf596e26550bb483236ae) for the Java Host, which outlines the objectives and roadmap for the next development stage. You can also see the codebase in our [GitHub repository](https://github.com/LimeChain/Fruzhin).
<br/>

### Milestone 0 - Block execution improvements

**Deliverables:**

| Number | Deliverable | Specification | Link to repository |
| --- | --- | --- | --- |
| 0a. | License | Apache 2.0 | - | [-]|
| 0b. | Documentation | Mostly inline documentation will be added. | [-]|
| 0c. | Testing and Testing Guide | A milestone further down the line handles the heavy integration runtime tests. Unit tests will be written. | [-]|
| 1. | Research | All possible solutions will require a certain amount of refactoring so making sure we taking the correct approach is mandatory. | [Task #355](https://github.com/LimeChain/Fruzhin/issues/355) |
| 2. | Abolish all Singletons related to the HostAPI | This will help us decouple the runtime calls. | [Task #375](https://github.com/LimeChain/Fruzhin/issues/375) |
| 3. | Decouple Spring and Polkadot Runtime | Right now we need a working Spring instance (with all of its components) to make ANY runtime call. These 2 shouldn’t be coupled so hard. | [Task #376](https://github.com/LimeChain/Fruzhin/issues/376) |
| 4. | Storage HostAPI functions remodelling | As storage access is one of the most important and slowest features, it would greatly help out node to have them remodelled so that trie root calculation can happen in parallel. | [Task #437](https://github.com/LimeChain/Fruzhin/issues/437) |

<br/>

### Milestone 1 - BABE

**Deliverables:**

| Number | Deliverable | Specification | Link to repository |
| --- | --- | --- | --- |
| 0a. | License | Apache 2.0 | - | - |
| 0b. | Documentation | In addition to inline documentation we will have a dedicated README file for the BABE protocol. |[-]|
| 0c. | Testing and Testing Guide | Multitude of unit tests will be written as opposed to integration tests which will be decided on a case by case basis. |[-]|
| 1. | Research and design | Gather the whole team and have them read and take part in the design meeting going over all the details for implementing the BABE algorithms. | [-]|
| 2. | Block authoring session key pair | Creation of said key pair is a necessary step for the block production lottery. | [Task #379](https://github.com/LimeChain/Fruzhin/issues/379) |
| 3. | Block Production Lottery | Implement the block production lottery algorithm as well as the underlying required functions and Runtime calls. | [Task #383](https://github.com/LimeChain/Fruzhin/issues/383) |
| 4. | Slot Number Calculation | Implement using NTP (Network Time Protocol) for now as the docs suggest it is currently the safer choice. | [Task #384](https://github.com/LimeChain/Fruzhin/issues/384) |
| 5. | Epoch Randomness | Implement the logic for getting the randomness seed through the Runtime and through consensus messages. | [Task #386](https://github.com/LimeChain/Fruzhin/issues/386) |
| 6. | Verify Authorship Right | Implement the algorithm as well as any underlying functions like Verify Slot Winner. | [Task #386](https://github.com/LimeChain/Fruzhin/issues/386) |
| 7. | Build Block | Implement the algorithm as well as any underlying functions with the exception of Median Algorithm as we will be using NTP instead. | [Task #387](https://github.com/LimeChain/Fruzhin/issues/387) |
| 8. | Invoke Block Authoring | Implement the algorithm as well as any underlying functions. Also announce the block once created. | [Task #388](https://github.com/LimeChain/Fruzhin/issues/388) |

<br/>

### Milestone 2 - GRANDPA

**Deliverables:**

| Number | Deliverable | Specification | Link to repository |
| --- | --- | --- | --- |
| 0a. | License | Apache 2.0 | - |
| 0b. | Documentation | In addition to inline documentation we will have a dedicated README file for the GRANDPA protocol. |[-]|
| 0c. | Testing and Testing Guide | Multitude of unit tests will be written as opposed to integration tests which will be decided on a case by case basis. |[-]|
| 1. | Research and design | Gather the whole team and have them read and take part in the design meeting going over all the details for implementing the GRANDPA algorithms. | [-]|
| 2. | GRANDPA GHOST | Implement the algorithm. | [Task #395](https://github.com/LimeChain/Fruzhin/issues/395) |
| 3. | Best Final Candidate | Implement the algorithm and update the GRANDPA GHOST algorithm. |[Task #396](https://github.com/LimeChain/Fruzhin/issues/396) |
| 4. | Best PreVote Candidate | Implement the algorithm. | [Task #397](https://github.com/LimeChain/Fruzhin/issues/397) |
| 5. | Finalizable | Implement the algorithm. | [Task #398](https://github.com/LimeChain/Fruzhin/issues/398) |
| 6. | Attempt to Finalize At Round | Implement the algorithm as well as any underlying functions. | [Task #399](https://github.com/LimeChain/Fruzhin/issues/399) |
| 7. | Initiate GRANDPA | Implement the algorithm which requires fully implementing Play GRANDPA Round algorithm as well as some smaller algorithms like Derive Primary. | [Task #400](https://github.com/LimeChain/Fruzhin/issues/400) |
| 8. | Forced authority set changes detection and handling | Implement logic behind the handling and detection of forced authority set changes. | [Task #401](https://github.com/LimeChain/Fruzhin/issues/401) |
| 9. | Catchup request sending | Implement logic for sending catchupo requests. | [Task #402](https://github.com/LimeChain/Fruzhin/issues/402) |
| 10. | Process Catchup request | Implement the algorithm as well as any underlying functions. | [Task #403](https://github.com/LimeChain/Fruzhin/issues/403) |
| 11. | Process Catchup response | Implement the algorithm as well as any underlying functions. | [Task #733](https://github.com/LimeChain/Fruzhin/issues/733) |
| 12. | Disable Validators | Faulty validators should be reported. | [Task #405](https://github.com/LimeChain/Fruzhin/issues/405) |

<br/>
[Task #388]()
### Milestone 3 - BEEFY

**Deliverables:**

| Number | Deliverable | Specification | Link to repository |
| --- | --- | --- | --- |
| 0a. | License | Apache 2.0 | - |
| 0b. | Documentation | In addition to inline documentation we will have a dedicated README file for the BEEFY protocol. |[-]|
| 0c. | Testing and Testing Guide | Multitude of unit tests will be written as opposed to integration tests which will be decided on a case by case basis. |[-]|
| 1. | Research and design | Gather the whole team and have them read and take part in the design meeting going over all the details for implementing BEEFY and clearing up the MMR structure. | [-]|
| 2. | BEEFY session key pair | Ensure the existing Secp256k1 functionality in the project is sufficient to produce a BEEFY session key pair and add whatever necessary. | [Task #815](https://github.com/LimeChain/Fruzhin/issues/815) |
| 3. | Create MMR | Create the MMR (Merkle mountain ranges) structure. This milestone objective will be further split into more granular tasks. |MMR structure is handled by the runtime logic. The host has no responsibility in generating an MMR proof related to BEEFY messages, but rather to gossip them to its peers.|
| 4. | Sign and gossip payload |  |[Task #776](https://github.com/LimeChain/Fruzhin/issues/776) |
| 5. | Committing witnesses  | The relayer should collect the gossiped votes. |The responsibility of collecting gossiped beefy votes and creating the witness structure is of the relayer node rather than the validator node.|
| 6. | Requesting signed commitments  | Light clients should be able to request signatures from the relayer |[Task #831](https://github.com/LimeChain/Fruzhin/issues/831) |
| 7. | Participate in BEEFY Consensus | Implement session, the logic for mandatory and non mandatory blocks, BEEFY round number algorithm, validate and broadcast votes. |[Task #775](https://github.com/LimeChain/Fruzhin/issues/775) |

<br/>

### Milestone 4 - Upgrading the Full Sync

**Deliverables:**

| Number | Deliverable | Specification | Link to repository |
| --- | --- |---| --- |
| 0a. | License | Apache 2.0 |
| 0b. | Documentation | Inline documentation.|[-]|
| 0c. | Testing and Testing Guide | Multitude of unit tests will be written as opposed to integration tests which will be decided on a case by case basis. |[-]|
| 1. | Implement block tree pruning | It’s necessary to have access to the pruned block tree for the correct execution of part of the following algorithms. |[Task #389](https://github.com/LimeChain/Fruzhin/issues/389) |
| 2. | Retrieve authorities from Runtime | Make the necessary Runtime calls to get the authority list. |[Task #390](https://github.com/LimeChain/Fruzhin/issues/390) |
| 3. | Add consensus message to header | In the case of a change to the authority list during a state transition we want to add an appropriate consensus message to the block header.  |[Task #391](https://github.com/LimeChain/Fruzhin/issues/391) |
| 4. | Complete the implementation of Import and Validate Block | Finish the algorithm by adding the Verify Authorship Right and Verify Block Justification algorithms to it and extract it to a separate function. Also announce the block to the network. |[Task #392](https://github.com/LimeChain/Fruzhin/issues/392) |
| 5. | Improve peer finding | Update Nabu dependency to latest version and ensure we can keep a two digit number of peers connected and synching at all times. Revisit log frequency/level after to avoid log clogging. |[Task #354](https://github.com/LimeChain/Fruzhin/issues/354) |
| 6. | Ensure network compatibility | Host is able to sync up to the head of the chain. Requires testing with all networks (polkadot, kusama, westend).  |[Task #393](https://github.com/LimeChain/Fruzhin/issues/393) |
| 7.  | Correctly load a block state  | We are currently saving a valid block state but lack the of getting it and using it which would save a lot of syncing time. |[Task #352](https://github.com/LimeChain/Fruzhin/issues/352) |
| 8.  | Improve syncing strategy | Test and adjust the synching strategy so that the reputation of the node stays as high as possible. A bit of research on node reputation is mandatory for this task.|[Task #353](https://github.com/LimeChain/Fruzhin/issues/353) |

<br/>

### Milestone 5 - Upgrading wasmer-java

**Deliverables**

| Number | Deliverable | Specification | Link to repository |
| --- | --- | --- | --- |
| 0a. | License | MIT |
| 0b. | Documentation | Greatly improve the README of the project by deleting obsolete information and restructuring it in a better way with also adding the latest functionality updates there as well. |[-]|
| 0c. | Testing and Testing Guide | Not much testing will be needed for the changes in this milestone. |[-]|
| 1. | Research and implement a way to release all necessary binaries | Java has no way of interacting with wasm files and therefore we are using native functions - in this case Rust which makes Fruzhin platform dependant. The best way to deal with this problem is to have binaries for different OS+Chip combinations but GitHub doesn’t offer apple runners for free. There are probably other ways we can have the ARM binaries be built and that would help up remove the manual setup process in Fruzhin. |[-]|
| 2. | Logging | Add an abundance of logs of different levels so that Runtime calls can more easily be tracked and debugged. |[Task #416](https://github.com/LimeChain/Fruzhin/issues/416) |
| 3. | Minor refactoring | There are a lot of parts in the code that could be refactored for better readability and effectiveness since they were written a long time ago with an older Rust version. |[Task #417](https://github.com/LimeChain/Fruzhin/issues/417) |

<br/>

### Milestone 6 - Compatibility, monitoring and Docker

**Deliverables:**

| Number | Deliverable | Specification | Link to repository |
| --- | --- | --- | --- |
| 0d | Docker | Make Fruzhin runnable via Docker. | [Task #418](https://github.com/LimeChain/Fruzhin/issues/418) |
| 1. | Set up Prometheus  | Add Prometheus metrics monitoring to Fruzhin. |[Task #417](https://github.com/LimeChain/Fruzhin/issues/418)|
| 2. | CLI arguments improvement | Ensure synchronisation between the CLI arguments used in polkadot to improve user experience. |[Task #420](https://github.com/LimeChain/Fruzhin/issues/420)|
| 3. | Ensure network compatibility | Make sure the node works the exact same way across all networks. Reinforce with tests. | [Task #421](https://github.com/LimeChain/Fruzhin/issues/421)|

<br/>

### Milestone 7 - Testing

**Deliverables:**

| Number | Deliverable | Specification | Link to repository |
| --- |---| ---| ---|
| 1. | Consensus integration tests  | Consensus is a very important part of the network and to make sure our authoring node is acting exactly the way it is supposed to. Therefore our team will add an abundance of integration tests in order to verify the behaviour. | [Task #422](https://github.com/LimeChain/Fruzhin/issues/422) |
| 2. | Runtime integration tests    | Add multiple integration tests which specifically focus on the Runtime class and Runtime exported functions.| [Task UNIT TESTS #424](https://github.com/LimeChain/Fruzhin/issues/921) |
| 3. | Integrate in cloud | Deploy Fruzhin to cloud. | [Task #424](https://github.com/LimeChain/Fruzhin/issues/424) |
|    | The Java Host Authoring Node has been deployed on GCP, while connectivity was tested locally on the Polkadot, Kusama and Westend networks. Recently we have encountered some unexpected issues and we are working together with Parity's engineers on potential fixes. | |
| 4. | Implement Todo.md changes    | We have a file in Fruzhin called Todo.md in which we have test and refactoring ideas. | [Task #425](https://github.com/LimeChain/Fruzhin/issues/425)  [Task #425](https://github.com/LimeChain/Fruzhin/issues/493)|

<br/>

### Milestone 8 - Documentation and article

**Deliverables:**

| Number | Deliverable | Specification | Link to repository |
|--------| --- | --- | ---|
| 0e     | Article | Publish an article about the new functionalities. | [Published an article on the Polkadot Forum.](https://forum.polkadot.network/t/our-java-host-fruzhin-evolves-to-authoring-capabilities/13706?u=limechain)|
| 1.     | Readme improvements | Improve the documentation and add a comprehensive guide of how to use the authoring node. | [-] |
| 2.     | Minor docs improvements | We will also revisit the documentation we’ve written so far and refactor it wherever necessary. | [-] |

<br/>

### Milestone 9 - Developer Relations

**Deliverables:**

| Number | Deliverable | Specification | Link to repository |
|---|---|--| ---|
| 1.     | Workshop                  | Host a workshop on how to use the authoring node.                                          | [-] |
| 2.     | Update educational videos | Update the videos about Fruzhin with he newly added functionalities.                       | [Link to video](https://drive.google.com/file/d/1MyPJhmOLSVJXk5GrjTDwQcCSNDk4RnVt/view) |
| 3.     | Gather feedback           | Use the community channel to gather feedback.                                              | [-] |
| 4.     | User issues support       | Dedicate time to address issues raised by users.                                           | A portion of the grant will be dedicated to addressing blocking issues identified by the community, aiming to ensure the stability of the Java host node for a period of 1-2 months post-progress report submission. Furthermore, we are evaluating the potential for a separate maintenance grant, which would be coordinated as necessary.|
| 5.     | Upgrade Host              | Upgrade the Host by improving on the parts which have received the most negative feedback. | [-] |

<br/>

### Milestone 10 - Research relaying node scope

**Deliverables:**

> After careful consideration, we've decided not to move forward with the next phase of this project, which means we won't be applying for the associated grant at this time. Our decision is driven by a thorough assessment of the project's evolving landscape and the significant challenges identified.

>One primary concern is the impending obsolescence of several key components essential for the project's functionality. With the JAM expected to go live in the near future, these components will become outdated, making our current proposed solution less viable and efficient in the long term. Investing in technology that will soon be obsolete doesn't align with our goals for creating sustainable and forward-looking solutions.

>Furthermore, our extensive research, combined with valuable insights gained from conversations with other implementers in the field, clearly indicates that the relay node is by far the most intricate and demanding phase of the entire host project. This particular stage presents substantial technical complexities and requires a significant allocation of resources. Our preliminary estimations, based on this research, suggest that Phase 4 alone could require approximately 1.5 to 2 years to complete. Given these substantial timelines and the inherent complexities, we've concluded that pursuing the next phase and the project grant at this juncture would not be a reasonable or efficient path forward. 




### Milestone 11 - **Light Client Web Scope**

> The milestone items listed here don’t correlate 1 to 1 with the ones in the proposal.  We have spoken with people from the foundation about small changes to this milestone.
You can find the codebase of the Web Java Host (Fruzhin) Light Client in the repository [here](https://github.com/LimeChain/Fruzhin-Web). Check out the first v1.0.1 release [here](https://github.com/LimeChain/Fruzhin-Web/releases/tag/v1.0.1).
**Deliverables**

| Number | Deliverable | Specification | Link to repository |
| --- | --- | --- | --- |
| 1. | WebAssembly integration | 1. Segregate Light Client part to be referenced/forked <br /> 2. Set up separate repository <br /> 3. Add a dependency to TeaVM and compile to WASM | [Run the wasm in the broswer #487](https://github.com/LimeChain/Fruzhin/issues/487) |
| 2. | P2P communication | 1. Set up communication with RPC calls as a standalone syste <br /> 2. Set up Kademlia DHT running in the web <br /> 3. Benchmark both variants and write a suitable structure of usage |[P2P #494](https://github.com/LimeChain/Fruzhin/issues/494), [P2P #495](https://github.com/LimeChain/Fruzhin/issues/495) |
| 3. | Diagnostics and issues support | 1. Announce usage in communication channel to start collecting user feedback <br /> 2. Benchmark against a locally running Fruzhin node <br /> 3. Address issues raised by users | [Announce Fruzhin Web Release v1.0.1](https://forum.polkadot.network/t/polkadot-java-based-node-host-implementation-updates-thread/8904/8?u=limechain) |
| 4. | Finalization | 1. Add comprehensive documentation <br /> 2. Add integration tests covering the most problematic cases <br /> 3. Research for next phase/improvements | [-]|
