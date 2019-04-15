# Understanding Stellar

It would be nuts to immediately dive into the code, therefore I found this high-level architectural overview guide on the Stellar website.

### API: Horizon

All interactions with the Stellar network happen through Horizon, a RESTful HTTP API server. It allows developers to submit transactions, check account’s balance, and subscribe to events. You can use Horizon through your web browser, a command line tool like cURL, or the Stellar SDK which is the easiest solution. The Stellar SDK is available for JavaScript, Java and Go. There are also community-maintained SDKs for Python, C#, and Ruby.

### Stellar Core

The Stellar Core is the backbone of the Stellar network, every Horizon server connects with it. The Stellar Core is responsible for validating transactions and reaching consensus. The core is run by a bunch of individuals creating a decentralized network. Each transaction on the network costs a small fee: 100 stroops (equal to 0.00001 XLM). The should prevent bad entities from spamming the network.

#### Stellar Consensus Protocol (SCP)

SCP opts for safety over liveness — in the event of partition or misbehaving nodes, it halts the progress of the network until consensus can be reached. You can find more information on the protocol in their whitepaper.

#### Run Stellar Core with Docker

It is possible to become part of the network by running a Stellar Core instance. Such an instance can be easily set up with stellar/quickstart docker image.

####Testnet

Luckily, Stellar provides a testnet for development purpose. Information can be found here.

