# Curriculum Structure

Information on the internet is increasingly abundant, but this does not
translate into more learning. On the contrary, a sea of disconnected information
makes it harder to discern what is most relevant at each stage of learning. A
sea of information is a treasure trove for those who have already built a
conceptual framework on a given subject, but it can serve as a factor of
cognitive overload for beginners.

Because of this, content curation and mentoring are considered the gold standard
of education. A structured curriculum helps the learner to focus on the
fundamental aspects of the subject while a mentor helps to identify and smooth
out the points of friction in understanding.

The problem is the cost of this scheme. It is not easy to find dedicated
mentors, they have limited time to dedicate to this activity and good mentoring
requires individual attention. Furthermore, not every potential learner is at
the right time to successfully benefit from the combination of a good curriculum
and dedicated mentors.

That is why the Bitcoin Dev Launchpad is structured in 3 phases, as a commitment
funnel in which each phase selects the best participants from the previous
phase. This way, we can increasingly commit resources to those participants who
demonstrate greater proof of work.

## Phase 1: Extended selection

A 4-week Socratic Seminar discussing the book Mastering Bitcoin, by Antonopolous
and Harding (https://github.com/vinteumorg/mastering-bitcoin-seminar), along
with a coding challenge (https://github.com/vinteumorg/task-test-the-test). With
the seminar, we hope to provide enough Bitcoin context to broaden the impact of
the following phases, while also identifying those programmers who seem
genuinely interested in the possibility of developing a career in open source
software. Even those that are not selected to the next phase will benefit from
participating in the cohort by deepening their understanding about the Bitcoin
protocol.

## Phase 2: Skillset Development

A 12-week curriculum built around developing three dimensions:
technical/programming skills, Bitcoin context, and open source development
culture. Self-study and socratic discussions continue in this phase, now
combined with a structured curriculum described next. The Bitcoin context and
technical skills are exercised through lectures and programming challenges
involving foundational problems the Bitcoin protocol tries to solve. Open source
culture is fostered with guided PR reviews and discussions with experienced open
source contributors.

### Week 1: Onboarding + Bitcoin Core

Discuss why Bitcoin and why open source.

**Programming challenge**: explore mainnet blockchain to get acquainted with bitcoin-core
(https://github.com/vinteumorg/task-rpc-scavenger-hunt).

### Week 2: Find your coins

Understand transactions, basic scripts, and segwit.

**Programming challenge**: given a private key and a signet blockchain, build a
wallet that scans the blockchain and retrieves your UTXOs
(https://github.com/vinteumorg/task-signet-wallet).

### Week 3: FOSS culture

Discuss open vs. closed source development models, open protocols, and
meaningful contributions (code review, issues, bug fixes, new features).

### Week 4: Spend your coins

Understand transaction signing and verification.

**Programming challenge**: given a private key and a signet blockchain, spend
some UTXOs the wallet found in week 2 challenge
(https://github.com/vinteumorg/task-signet-wallet).

### Week 5: PR Review Club

Understand how to meaningfully review PRs guided by an experienced contributor.

### Week 6: P2P networking

Understand the basics of networking and the Bitcoin protocol messages.

**Programming challenge**: Establish a connection with a public Bitcoin node
(handshake) and get block headers ([WIP]
https://github.com/vinteumorg/devel-task-networking)

### Week 7: Open source projects presentations

Learn about the Bitcoin ecosystem of open source projects by interacting with
the maintainers or frequent contributors.

### Week 8: Build a block

Understand the blockchain role in the protocol, block headers, merkle roots and
the proof of work mechanism. 

**Programming challenge**: given some transactions, build and mine
a valid block ([WIP] https://github.com/vinteumorg/devel-task-mining)

### Week 9: Contribute to an open-source project

Start working on open source contributions with support of the program's mentors
and instructors.

### Week 10: What's next

At this point, participants should have get a comprehensive understanding of the
Bitcoin base protocol. Now, we introduce the many layers built upon it like the
Lightning Network, Cashu, Fedimint, Ark, etc.

### Week 11: Hackathon

Build something or make meaningful contributions to an open source project.

### Week 12: Hackathon + Offboarding

Show your work and evaluate the program.

## Phase 3: Fellowship

It would be naive to believe that a 12-week curriculum will be enough to train
an accomplished open source contributor. After all, frequent contributors are
exactly that, people that keep contributing and develop authority and project
ownership over an extended time framea. Inspired by the [Summer of
Bitcoin](https://www.summerofbitcoin.org) initiative, we provide a six-month
scholarship to incentivize the top performers to keep working on an open source
project.

Each grantee will be assigned a mentor whose job is to motivate meaningful
contributions, keep the mentee accountable, and assess their performance to
assist Vinteum's board in recommending a regular full time grant or seek an
international grant. In this way, we aim to alleviate the financial burden and
the solitude reported by open source developers during their transition from
traditional careers.

