# Milestone Delivery :mailbox:

* **Application Document:** <https://github.com/pioneersprize/Polkadot-Pioneers-Prize/blob/main/applications/reed-solomon-perf.md>
* **Milestone Number:** 1

**Context** 
> Please provide a short paragraph or two connecting the deliverables in this milestone and describing their purpose.

A set of code changes that enables primarily `avx2` based `SIMD` acceleration and adding sufficient tests. As part of this, also re-commission the perf measurement pipeline.

**Deliverables**

| Number | Deliverable | Link | Notes |
| ------------- | ------------- | ------------- |------------- |
| 1. | SIMD perf | <https://github.com/drahnr/reed-solomon-novelpoly/pull/1> respectively <https://github.com/paritytech/reed-solomon-novelpoly/pull/10> | Due to a lack of permissions I had to target my own fork for the pipeline runs |
| 2.  | CI pipeline | <https://ci.fff.rs/teams/main/pipelines/reed-solomon> |  |

**Additional Information**

This is the only pre-requisite to be able to start work on <https://github.com/pioneersprize/Polkadot-Pioneers-Prize/pull/10> but also to get the work merged.

Jeff B. already did a review pass <https://github.com/drahnr/reed-solomon-novelpoly/pull/1#issuecomment-1715371561>
