## CAP theorem
> <b> In the presence of network partition, one has to choose between consistency and availability (tradeoff). </b>

* <b>Consistency</b>: Every read receives the most recent write or an error
* <b>Availability</b>: Every request receives a (non-error)response - without the guarantee that it contains the most recent write
* <b>Partition tolerance</b>: The system continues to operate despite an arbitrary number of messages being dropped(or delayed) by the network between nodes

### Consensus
All non-faulty processes decide the same value(data consistency)

#### Model
* synchronous model 
* asynchronous model

### Fischer-Lynch-Paterson (FLP) result：
> You can't do agreement in an AsynchronousMessagePassing system
> if even one crash failure is allowed, unless you argument
> the basic model in some way, e.g. by adding randomization or failure detectors.

### Challenge
* faulty processor
* <b>Byzantine faults</b>, weakest type of failure and the most difficult kind to deal with. Allow arbitrary failures including malicious faults
    1. failure to return a result
    1. return of an incorrect result
    1. return differing results to different parts of the system
    
## Solutions?
    
### Common fault tolerant (unreliable processors, no malicious processors)
* Paxos
* Raft

### Byzantine fault tolerance (Byzantine Generals' Problem, arbitrary failures)

* Byzantine Paxos
* Practical Byzantine Fault Tolerance Algorithm (PBFT) 


Proof Of Work
---
1. [Bitcoin POW]
1. [Cuckoo Cycle](https://github.com/tromp/cuckoo) adopted by aternity
1. [Equihash](https://github.com/tromp/equihash) adopted by Zcash

Proof Of Stake
---
1. [Ethereum Casper](https://github.com/tromp/equihash)
1. [Delegated Proof of Stake](http://docs.bitshares.org/bitshares/dpos.html)
1. [Cardano Ouroborous](https://www.cardano.org/en/ouroboros/)
1. [Algorand](https://eprint.iacr.org/2018/377)
1. [Tendermint](https://tendermint.com/)