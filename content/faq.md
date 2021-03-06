---
title: FAQs
geekdocBreadcrumb: false
aliases: ["/faq", "/about/faq"]
---

{{< expand "How many transactions can rubix handle?" >}}

Popular blockchains (BTC and ETH) work by every node adding transactions to a central chain and the chain grows in one direction with it.  Rubix is designed and built as a peer to peer blockchain where a transaction happening from node A to node B is only corresponding quorum nodes are only known and participated in the transaction. Maximum transaction threshold with 10,000 nodes is 150,000. As more sender, receiver, and quorum nodes are joining the network, maximum transactions that happen in the network also increase.  Rubix is truly peer to peer and decentralized - transaction speed or throughput grows with the network and not locked to value. Rubix is a distributed blockchain and bitcoin is a centralised blockchain in that say Today with around 100 transactions / per minute with a current number of 12,000 nodes. An argument is with current industry standard by web2 services, this is not a big number. 10,000 is also not a bug number. With the number of nodes growing as with time, Rubix will be scaling larger than any datacenter, securely with 0 transaction fee.

{{< /expand >}}

{{< expand "Becoming part of the network?" >}}

You can setup a rubix node in any decent spec laptop in 2022. You can also setup a rubix node in a server with a dedicated server. You can also setup a rubix node in a cloud VM. Follow this will creating DID for your node in the network. DID is the identity of your node in the network to do transfers or to become a validator.

{{< /expand >}}

{{< expand "How to create a DID?" >}}

{{< /expand >}}

{{< expand "How much does it cost to setup a node?" >}}

{{< /expand >}}

{{< expand "How a token is transfered?" >}}

In cryptocurrency, “token” is often used as a synonym for “cryptocurrency.” Often the two terms are combined and the term “cryptocurrency token” is used. Cryptocurrencies exist as tokenized data (a type of encrypted data used in both cryptocurrency and computer security in general), therefore cryptocurrencies are often called tokens.

All Rubix nodes join the  network to conduct transactions with each other. A transaction can be :
A digital contract that involves exchanges of services or goods in return for exchange of other services or goods
A digital contract that involves exchange of services or goods for exchange of any medium of value such as fiat currency or simple transfer of native token
At any given moment, several peer-to-peer transactions are submitted to the Rubix network, transactions are processed parallely independent of each other unless the transaction involves common peers. A transaction is initiated by one peer node.
To initiate the transaction, the peer node must use at least one RBT token. Depending on the RBT token used by the peer node to initiate the transaction, the transaction is added to the corresponding Proofchain

Sender will request the advisory node a list of quorum list(24) which are online. The sender will ping each members of the quorum
Inorder for token tranx or to transfer a token(s) from one wallet to another the following curl command will be used:
$ curl --header "Content-Type: application/json" --request POST <http://localhost:1898/initiateTransaction> --data '{ "receiver": "445f59c3d71c6769124470cf4b82ca0b9b1626aec4f14f50a8f1e6a13e1fc70d", "tokenCount":1, "comment":"transaction comments", "type":1}'
Request Type: POST
Port: 1898
Input: receiver (String), tokenCount (Integer), comment (String)
Returns: Transaction ID (String), Success / Failure (Boolean), DID (String)

{{< /expand >}}

{{< expand "What are Levels and Credits? How to earn required Credits to mine an RBT?" >}}

Each of the 15 successful validators (5 out of 7 ⍺ validators following PBFT consensus, 5 out of the 7 β, 5 out of the ) in any transaction receive one proof credit (p). For a transaction involving an asset token, ⍺ validators get an additional proof credit each (more on this in the asset transfer section later in this paper).Validators will accumulate proof credits from various transactions across different Proofchains. When a node’s (p) reaches the threshold level , the node can convert the proof credits into one new RBT token. Nodes continue to earn proof credits & thereby harvest new RBT tokens by participating in consensus of various transactions & perpetually storing the consensus proofs. When a node transfers its outstanding proof credits or the harvested RBT tokens along with the supporting proof credits to a new node, the receiving node will continue to store the transaction proofs (otherwise the corresponding RBT token will be invalid).

Each validator node keeps the latest count of outstanding proof credits as well as the number of RBT tokens they have validated in various transactions by pledging the proof credits. New transacting nodes use net outstanding proof credits data to select the ⍺ validators. The authenticity of the proof credits & pledge count is confirmed by PBFT consensus among the 𝝰 validators.

{{< /expand >}}

{{< expand "Do I need to backup my node after every transaction or periodically?" >}}

Rubix is designed differently from other chains, its more decentralized.  Other chains, everyone data is stored everywhere, causing privacy issues/slow adoption.  We designed it such that everyone is responsible for their data, but provenance is on the chain & immutable.

If a transaction happens after last backup & system crashes, you can restore to latest state by syncing proofchain to any node that did txns after your node txn.  Because every subsequent node will store the latest chain.  So you can always sync to the latest state.  That's not an issue if you are using a backup.

{{< /expand >}}

Have more questions? Feel free to Tweet or message our team [@rubixchain](https://twitter.com/rubixchain)
