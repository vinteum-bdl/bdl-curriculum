# Vinteum FOSS Program

## Why Bitcoin?

Bitcoin is a collection of concepts and technologies that form the foundation of a new ecosystem for money. Its major innovation is the ability to create an emergent consensus system on an open platform. Emergent because consensus is not explicitly reached; there is no fixed or electoral mechanism in space and time where consensus happens. In fact, this consensus is the product of  asynchronous interactions between thousands of independent agents, each following a set of relatively simple rules—rules that are decided by the agents themselves. All of Bitcoin's properties, including its ability to function as currency and as means of payment, as well as its security model, do not rely on trust in a central authority but are derived from the very decentralized consensus mechanism that the network achieves about the state of value balances on the network.

This ethos of decentralization is reflected in numerous aspects of the Bitcoin ecosystem. Since each agent in the system can decide its own rules, each one can build its own implementation of the software artifacts it will use. When viewed globally, the consensus mechanism is quite resilient to the individual actions of each node in the network, but [the local state of each node is quite sensitive](https://learnmeabitcoin.com/technical/blockchain/hard-fork/) to the [minutiae of the rules it implements](https://bitcoinmagazine.com/technical/bitcoin-network-shaken-by-blockchain-fork-1363144448). Therefore, although each node is free to run its own implementation of the protocol, it is estimated that [more than 98%](https://blog.lopp.net/when-do-bitcoin-node-operators-upgrade/) of [the nodes in the network run](https://bitnodes.io/dashboard/8y/#user-agents) the [Bitcoin Core](https://github.com/bitcoin/bitcoin) client[^1].

[^1]: [Be careful when reading statistics about Bitcoin.](https://jimmysong.medium.com/why-bitcoin-node-statistics-arent-trustworthy-5882d9a9d2bf)

The Bitcoin Core project was launched by Satoshi Nakamoto in 2009 and has been maintained exclusively by the community since his disappearance in 2010. It is a complex project developed under an open-source model, whose [governance](https://pierre-rochard.medium.com/bitcoin-governance-37e86299470f) reflects the decentralized ethos of the network. Bitcoin Core is a focal point for Bitcoin protocol development, but it does not function as a command and control center. Anyone is free to propose changes to the code, from small bug fixes to major changes in the consensus rules (hard and soft forks). Anyone is free to review the changes and provide feedback; there is no gatekeeper or certification required to contribute to Bitcoin Core. When a contribution seems to have addressed all reasonable objections raised during the review, a maintainer will merge it with the main codebase. Maintainers act as janitors of the code repository, and even their own projects undergo the same review process as any other contributor's.

However, Bitcoin Core is only a (reference) implementation of the Bitcoin protocol. Since it is an open, permissionless protocol, the Bitcoin protocol serves as a development platform for various other protocols aiming at different applications, built upon the guarantees provided by the base system (first layer). Examples of these protocols include:

- the Lightning Network, a micropayment protocol that seeks to increase Bitcoin's scalability through a network of bidirectional payment channels without delegating the custody of funds;
- Cashu, an ecash protocol that uses Bitcoin as a means of settlement;
- Fedimint, a protocol for the custody and transaction of Bitcoin in a federated (community) context;
- the Liquid Network, a protocol for issuing digital assets such as stablecoins, security tokens, and other financial instruments;
- Taproot Assets, a protocol for issuing digital assets that can be transferred via the Lightning Network;
- Ordinals, Inscriptions, and Runes, protocols for creating non-fungible tokens (NFTs) on the Bitcoin blockchain;
- BitVM, a computing paradigm capable of expressing Turing-complete smart contracts that uses the Bitcoin protocol to verify the state of computation;
- Stratum V2, a protocol for the distribution of work and coordination of miners on the Bitcoin network.

All of these examples are developed as open protocols with reference implementations created under an open-source model. Additionally, there is a need to develop tools so that users can interact with these applications in the form of wallets, clients, servers, signing devices, and more.

The Internet was built on open protocols, and this is what allowed humanity to unleash its full creativity to produce an unimaginable range of applications, many of which we are still trying to understand (like social networks). We believe that Bitcoin has the potential to be the [Internet of Money](https://www.amazon.com.br/Internet-do-Dinheiro-Andreas-Antonopoulos/dp/8585265000), an open platform for innovation that establishes a form of distributed consensus. Money is only its first application.

### Why Open Source?

The great challenge across different branches of engineering is how to manage the complexity of projects. The most successful technique is abstraction, which involves encapsulating certain functional parts within well-known interfaces. Hiding the implementation details of a mechanism behind black boxes allows the engineer to treat these parts as fundamental units, reducing complexity by concealing the details. In fact, this is a natural human ability: when driving a car, we don't concern ourselves with all the knowledge required to make that machine work. Instead of dealing with all the physics involved in the movement of these machines, we interact with a quite simple interface composed of a steering wheel, a few pedals, and levers.

The software industry is probably the one that most stresses the concept of abstraction. Once someone solves a software problem, it's very easy to encapsulate that solution in a software library and use it as a dependency in a more complex project. The C language was (and still is) so successful partly because it was the first to provide the ability to encapsulate reusable code libraries conveniently. Modern languages seek to improve this experience with tools like cargo (Rust), npm (JavaScript), pip (Python), and others, which help in distributing these libraries. The availability of extensive software libraries makes the entire industry more productive as developers don't need to solve the same problems repeatedly, gradually advancing the complexity of projects.

The convenience and necessity of using abstractions for building software projects align very well with the open-source development model. The decentralization promoted by the open-source model allows people to decide locally which problems they consider interesting and important to solve, as well as the technical approach they will use. People themselves can decide locally which of these projects should thrive through their adoption or abandonment. The ease of distribution and reuse of these solutions tends to accelerate this process, leading us to the current state of affairs where practically no software project exist that do not use components developed and distributed as open-source.

Bitcoin is a recent chapter in this story, which we believe will be another foundation for future applications. Working with open source is not only important because some of these projects are cornerstones of the industry and need maintenance, but it is also a software philosophy that allows truly innovative ideas to be proposed, tested, and eventually integrated into the ecosystem. Taking care of open-source projects is a way of taking care of the present, but it is also a way of taking care of the future.

As much as the open-source development model is a driver of innovation and accelerated industry advancement, sometimes economic incentives become distorted or simply do not seem to work correctly to provide the necessary resources for maintaining important projects. [Open-source projects tend to develop basic infrastructures and libraries](https://daniel.haxx.se/blog/2022/01/17/enforcing-the-pyramid-of-open-source/) whose users are other developers. In contrast, projects closer to non-technical users tend to be developed by companies within the corporate closed-source model, where most developers build their careers.

![All Modern Digital Infrastructure|450](https://imgs.xkcd.com/comics/dependency_2x.png)

The advantage of the open-source model is that it ends up being more resilient in the long run, even though this is a counterintuitive conclusion: "While commons may not be as profitable as companies, they are also more resilient because the currency of their transactions is the desire to participate, not money." (Nadia Eghbal, _Working in Public: The Making and Maintenance of Open Source Software_). We tend to believe that if Bitcoin were a company project, it probably would not have had the success it has had so far.

However, because they are further away from monetization sources, open-source projects often suffer from [a lack of resources](https://words.filippo.io/professional-maintainers/), whether it be [funding for maintenance work](https://github.com/zloirock/core-js/blob/master/docs/2023-02-14-so-whats-next.md) or [skilled developers](https://medium.com/@amitiu/onboarding-to-bitcoin-core-7c1a83b20365) capable of [making significant contributions](https://jimmysong.substack.com/p/how-do-i-contribute-to-bitcoin-core), especially when it comes to [project maintenance](https://jonatack.github.io/articles/on-reviewing-and-helping-those-who-do-it). The Bitcoin ecosystem has reasonable [funding sources](https://f.hubspotusercontent20.net/hubfs/5507270/AVAX%20-%20June2021/Giving%20Back%20to%20Bitcoin%20Ebook_July%202021.pdf) through grants[^2][^3][^4][^5][^6][^7][^8][^9][^10], companies that employ protocol developers, and other institutions[^11], but [it suffers from the same risks](https://adamjonas.com/bitcoin/funding/funding-bitcoin-development/).

[^2]: https://www.kraken.com/features/grants
[^3]: https://spiral.xyz/
[^4]: https://hrf.org/devfund
[^5]: https://developergrant.okcoin.com/
[^6]: https://brink.dev/programs
[^7]: https://maelstrom.fund/bitcoin-grant-program/
[^8]: https://vinteum.org/
[^9]: https://blog.bitmex.com/grants/
[^10]: https://opensats.org/
[^11]: https://chaincode.com

## Who?

Vinteum is a non-profit Bitcoin research and development center founded by Brazilian bitcoiners. The organization's mission is to promote the Bitcoin ecosystem in Brazil by providing grants to open-source developers, supporting in-person Bitdevs meetups in various cities, hosting online Chaincode-like seminars, and fostering debates and knowledge sharing within its community. Vinteum maintains a physical hackerspace in São Paulo, where it conducts workshops and technical courses and brings together the local developer community for collaboration and mentorship.

### Why a Brazilian program?

Other programs around the world:

- Chaincode: Global.
- Btrust Builders: Africa.
- Bitshalla: India.
- Libreria de Satoshi: Latin America.

<!-- Only [5% of the Brazilian population aged 16 to 24 wrote computer programs in the last year](https://goingdigital.oecd.org/datakitchen/#/explorer/1/toolkit/indicator/explore/en?mainCubeId=OECD.STI.DEP%2FDSD_ICT_HH_IND%40DF_IND&pairCubeId=&sizeCubeId=&mainIndId=H1K_I&pairIndId=&sizeIndId=&mainBreakdowns=AGE%3AY16T24.SEX%3A_T.EDUCATION_LEVEL%3A_T.INCOME_GROUP%3A_T.EMP_STATUS%3A_T&pairBreakdowns=MEASURE%3AALL&sizeBreakdowns=&lollipop=SEX&lollipopOpts=F.M&countries=&countryFilter=false&time=1104544800360.1672542000360&chart=barchart&fontSize=16&palette=normal&lastDates=true&timeScale=A&mainUnit=PT_POP&pairUnit=100HB&sizeUnit=&flip=false&fullLabel=true). Around 6% when considering the population aged 25 to 54 years. (Relevant data?) -->

<!-- ![[assets/20240727_programadores_jovens.png]] -->

- Identification: It is easier to create bonds, learn, and collaborate with people who are culturally closer to us.
- Providing a channel for other talents to thrive in the ecosystem by supporting the development journey of others (a good teacher is a multiplier of a message).

## What?

An educational program to **identify and train open-source developers** for the Bitcoin ecosystem.

### Program Objectives

The program aims to produce the following benefits for the Bitcoin ecosystem:

- Identify and train grantees for Vinteum or international organizations.
- Promote the creation of new businesses and companies based on Bitcoin in Brazil.
- Increase the number of developers working with Bitcoin in companies or open-source projects.
- Encourage new open-source projects that solve problems within the Bitcoin ecosystem.
- Train individuals capable of evangelizing programmers for the Bitcoin ecosystem in Brazil.
- Foster donations for the development of the Bitcoin ecosystem in Brazil.

Program alumni may produce beneficial side effects for the ecosystem, though they are not considered program objectives:

- More people “investing” in Bitcoin. We understand that Bitcoin is a tool for sovereignty and individual freedom, not a vehicle for investment or financial speculation. However, we expect that people will use this freedom to thrive by solving problems.
- “Better” regulation of Bitcoin. We believe that the best regulation of the technology is that which is spontaneously produced by the technology’s users making decisions in the market process. On the other hand, we understand that economic activity will continue to be regulated by the government for a long time. Understanding how Bitcoin technology works may lead to less harmful regulatory mechanisms than those currently in place.

**All of these are value propositions for the Bitcoin ecosystem. What is the value proposition for the individual participating in the program?** These value propositions are important for attracting the right students to the program.

We aim to achieve these objectives through the training of skilled individuals. The value proposition for participants in the program includes:

- **Working for purpose**, whether in a company developing a Bitcoin-based product, through grants for developers contributing to open-source projects, or by solving intellectual challenges or conducting research.
- **Developing technical skills**. The development of the Bitcoin protocol and other associated protocols involves knowledge across various computer science disciplines (data structures and algorithms, cryptography, networks, distributed systems, programming languages, databases, memory and hardware resource management). It is a complex and large-scale system that presents challenges for developers at all stages of their careers.
- **Participating in decision-making** about the future and maintenance of the Bitcoin protocol, either directly in protocol developer discussion forums (IRC[^12], email lists[^13], discussion forums[^14][^15], technical conferences[^16][^17][^18][^19][^20], meetups), or indirectly by discussing issues and pull requests in the repositories where software implementations are developed.

[^12]: https://web.libera.chat/#bitcoin-core-dev
[^13]: https://groups.google.com/g/bitcoindev
[^14]: https://delvingbitcoin.org/
[^15]: https://bitcointalk.org/
[^16]: https://x.com/satsconf_
[^17]: https://x.com/TheBitcoinConf
[^18]: https://x.com/tabconf
[^19]: https://x.com/btcplusplus
[^20]: https://x.com/advbitcoin

## When? 


## How?

### Program Structure

An open-source developer needs skills in three dimensions:

- **Technical Skills.**
- **Bitcoin Context.**
- **Open-Source Development Culture.**

Each of these dimensions will be addressed through a track in the program. The technical skills dimension will be covered diffusely through practical activities as well as in other tracks. This is not a programming course.

**Target Audience:** Programmers with technical skills. This is not a program for beginners.

#### Technical Skills

- **Systems Programming:** Memory management
- **Testing**
- **Command-line tools.**
- **Software repository management (git).**
- **Systems Programming:** Advanced knowledge in distributed systems, memory management, etc.
- **Quality and Security:** Solid knowledge in software development quality and security, including automated testing, CI/CD, code review processes, etc.

#### Bitcoin Context

The Bitcoin protocol consists of several moving parts that together form a harmonious whole. It is essential to understand the problems these pieces are trying to solve, as well as the trade-offs and engineering decisions involved in building the system. In this way, a developer will be able to understand the security guarantees provided by the Bitcoin network and use them to build other layer-two protocols that address additional issues associated with digital currencies and other applications.

##### Basic Aspects of the Protocol

**Transactions** are data structures that encode the transfer of value between system participants. They are the most crucial elements of the system. The rest of the protocol is designed to create, propagate, validate, and record transactions in the global ledger (the blockchain).

- Keywords: public and private keys, addresses, script, validation, digital signature, serialization.

**The blockchain** is a data structure that represents the consensus on the order in which transactions occurred within the system. It models time from the perspective of network participants and provides a mechanism for each participant to synchronize their local view of the network state with others. Satoshi himself used the term "timestamp server" to refer to this data structure.

- Keywords: blocks, proof of work, mempool, Merkle tree, Merkle root, mining, coinbase.

**The peer-to-peer network** is the chosen architecture for participants to communicate with each other.

- Keywords: packets.

The basic elements of the Bitcoin protocol offer various guarantees[^21]:

- **Absence of double-spending**: Ensures that no UTXO can be spent twice in the same valid blockchain.
- **Immutability of transactions**: Once written to the blockchain and a sufficient amount of proof of work has been built by network participants.
- **Neutrality**: Guarantees that network nodes will propagate valid transactions regardless of their origin.
- **Secure timestamping**: Since blocks have a predefined range of valid timestamps.
- **Authorization through digital signatures**.
- **Auditability**: As all transactions are public and can be analyzed by any network participant.
- **Accountability**: As the input value of each transaction must equal or exceed the output value, preventing new bitcoins from being created in regular transactions.
- **Validity of transactions**: A valid transaction remains valid in the future unless its inputs are spent by another transaction.
- **Integrity**: Altering the outputs of a transaction invalidates the signatures used to authorize the spending, thus invalidating the transaction.
- **Atomicity of Bitcoin transactions**: They are either valid and confirmed or not; there is no notion of partial transactions in the network.
- **Discreteness and indivisibility of transaction outputs**: Outputs can only be spent in their entirety.
- **Multi-signature UTXO control**: Allows creating quorums requiring multiple digital signatures.
- **Time locks**: Transactions can have time constraints determining when they become valid.
- **Existing and validated UTXOs**: A transaction can only spend existing and validated UTXOs, protecting against counterfeiting.
- **Blockchain consistency**: It is exponentially harder for reorganizations to occur in the network under certain non-partitioned computational power assumptions.
- **Commitment to external values**: Transactions can commit to external values by storing arbitrary data within certain limitations.
- **Predetermined and fixed monetary policy**.

[^21]: Antonopoulos, Andreas M., and David A. Harding. _Mastering bitcoin_. " O'Reilly Media, Inc.", 2023.

##### Basic Aspects of Lightning Network

These guarantees serve as security primitives that can be used to build other applications on top of the Bitcoin base protocol. The main one is the Lightning Network, a peer-to-peer micropayment network that aims to solve Bitcoin's scalability problem by implementing the concept of payment channels. A payment channel is a UTXO controlled by two participants in the Bitcoin network, where each contributes liquidity to the channel by committing funds on the Bitcoin network. Once the payment channel is established, participants can exchange transactions privately, without propagating these transactions to the rest of the network. The Lightning protocol provides various guarantees to ensure that participants can close the payment channel and recover their respective balances, as well as to penalize the channel counterpart by seizing the entire channel balance if it attempts to perform any illegitimate actions.

#### Open-Source Development Culture

- **Governance:** Who decides the work to be done and what will be incorporated into the project?
    - PR Merging: Bug fixes, new features
    - Consensus (rough consensus)
- **Quality:** How to maintain a high standard of software quality?
    - Code review, feedback

### Schedule and Description of Proposed Activities

#### Pre: Candidate selection
- Subscription form (Google Forms)
	- Name
	- Email
	- Github handle
	- Knowledge level about bitcoin
	- Expectations, why do you want to join the program?

Challenge: https://github.com/vinteumorg/task-test-the-test
- Goal: filter those not interested in putting a minimal effort, install dependencies and build Bitcoin Core, prepare the command line tools for the program.
- Deadline: 1 week.

#### Week 1 (Practice): Onboarding + Bitcoin Core command line
Lecture
- Why Bitcoin?
- Why Open Source?
- Administrivia
	- Program goals
	- Timeline of challenges and lectures
- Methodology
	- Weekly lectures: meant to accelerate, not to cover everything
	- Weekly office hours: meant to help get people unstuck and accountable
	- Recommended readings.
- Communications: Discord Server

Challenge: https://github.com/vinteumorg/task-rpc-scavenger-hunt
- Goal: warm-up, play with bitcoin core and the blockchain, have questions.

Reading material
- Bitcoin Whitepaper
- Mastering Bitcoin, chapters 2 and 3

#### Week 2 (Bitcoin): Find your coins
Lecture:
- Transactions
- Script 101: p2pkh, p2sh
- Segwit 101: p2wpkh

Challenge: https://github.com/vinteumorg/task-signet-wallet
- Goal: understand the transaction data structure, understand the basic mechanics of authentication (public keys) and authorization (digital signatures), understand what's an UTXO.

Keep a signet running: adapt https://github.com/btcfoss-career/signet-wallet-project-edilmedeiros

Reading material
- BIP 32
- BIP 141 (segwit)
- Mastering Bitcoin, chapters 5 and 6

#### Week 3 (FOSS): FOSS culture
Lecture:
- Open vs. closed source models
- Open protocols
- Contributions: issues, code review, bug fixes, new features
	- How to code review: concept -> approach -> code

Reading material

#### Week 4 (Bitcoin): spend your coins
Lecture:
- ECC 101: signing and verifying
- Transaction serialization and signing

Challenge: https://github.com/vinteumorg/task-signet-wallet
- Goal: deeply understand transactions by building and signing, understand what does it mean to own a bitcoin (be able to locate funds, be able to build and sign a spending transaction)

Reading material
- BIP 143 (Transaction Signature Verification for Version 0 Witness Program)
- Mastering Bitcoin, chapters 7 and 8

#### Week 5 (FOSS): PR Review Club
Lecture
- PR Review Club

Reading material
- Stuff related to the PR to be discussed.

#### Week 6 (Bitcoin): Build a block
Lecture
- Blockchain function: network clock (timestamp server)
- Block header
- Proof of work
- Merkle root

Challenge: https://github.com/vinteumorg/devel-task-mining
- Goal: understand what's the blockchain, understand proof of work, understand the Merkle root.

Reading material
- Mastering Bitcoin, chapters 11 and 12

#### Week 7 (FOSS): PR Review Club?
Lecture
- PR Review Club

Reading material
- Stuff related to the PR to be discussed.

#### Week 8 (Practice): Networking
Lecture
- Bitcoin network messages
- Bitcoin handshake, version + verack messages
- getheaders + headers messages

Challenge: https://github.com/vinteumorg/devel-task-networking
- Objetivo: Estabelecer conexão com um peer da rede (handshake), receber block headers (bloco genesis da signet)

Reading material:
- Programming Bitcoin, chapter 10

#### Week 9 (FOSS): PR Review Club?
Lecture
- PR Review Club

Reading material
- Stuff related to the PR to be discussed.

#### Week 10 (Bitcoin): Linha de comando LND?
- Objetivo: abrir um canal de pagamento, pagar um invoice.

Adaptar: https://github.com/btcfoss-career/lightning-scavenger-hunt-edilmedeiros

#### Week 11 (Practice): Hackathon
Build something

#### Week 12 (Practice): Hackathon
Build something

- Offboarding
	- Where to look for funding. Do we have examples of proposals we can show?
	- Help choose projects to work on/mentoring.
	- Point to learning opportunities outside of the program.
	- Alumni group
- Program evaluation and feedback from students

### Operational

#### Infrastructure
1. Full node with `txindex` enabled and running on a public IP. Setup [RPC proxy](https://github.com/vinteumorg/infra-rpc-proxy) to give students access.
2. [Signet server](https://github.com/vinteumorg/infra-signet-server) on a public address.
3. [Github Classroom](https://classroom.github.com/classrooms)

#### Communication media
- [Vinteum Discord Server](https://discord.gg/uTHhQX6g)
- Weekly lectures: Vinteum Google Meet
	- Create calendar events in advance


---

Papel dos mentores
- beta test dos challenges.
- review das entregas dos participantes.
- disponibilidade para tirar dúvidas no discord.
- auxiliar no sysadmin dos servidores.
- eventualmente, lecture.

Papel dos instrutores
- elaborar os challenges.
- review das entregas dos participantes.
- disponibilidade para tirar dúvidas no discord.
- sysadmin dos servidores.
- gerenciar github classroom.
- lectures



---

Funding
- Empresa
- Pre-mining/ICO
- Grants

https://f.hubspotusercontent20.net/hubfs/5507270/AVAX%20-%20June2021/Giving%20Back%20to%20Bitcoin%20Ebook_July%202021.pdf


Como posso contribuir?
- Contribuição direta: revisão de código, bug fixes, novas funcionalidades.
- Educação: é o objetivo deste programa e de todas as outras ações da Vinteum.
- Construindo um produto
- Doação: doar diretamente para um desenvolvedor ou para uma organização que financia grants.

Benefícios do programa

---
### Público-alvo
Níveis de consciência
- Não entendo de Bitcoin nem sei programar.
- Sei programar, mas não sou profissional, não entendo de Bitcoin.
- Sou programador junior, não entendo de Bitcoin.

#### Objeções
Não tenho tempo para participar.
	Arranje tempo.

Não sei programar em… 
	Você pode aproveitar para aprender uma nova linguagem.

Não sinto segurança em trabalhar por esmola, prefiro um emprego tradicional.
	Ainda assim, você pode se beneficiar do programa.


### Target Audience

**Levels of Awareness**

- I don't understand Bitcoin and I don't know how to program.
- I know how to program but I'm not a professional and I don't understand Bitcoin.
- I'm a junior programmer and I don't understand Bitcoin.

#### Objections

I don't have time to participate. Find time.

I don't know how to program in… You can use this as an opportunity to learn a new language.

I don't feel secure working for free, I prefer a traditional job. You can still benefit from the program.


