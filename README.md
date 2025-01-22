# Bitcoin Dev Launchpad by Vinteum

Developing a traditional career in software development is the natural path for
most programmers. Yet, we interact with many talented people who we belive could
be developing self-driven open source careers. Our growing community of
Brazilian Bitcoin developers makes us believe there are many more gifted
Brazilian and other Portuguese-speakers devs who could contribute to
critical projects while developing more fulfilling careers.

The Bitcoin Dev Launchpad (BDL) program is a 40-week program with the goal to
provide a solid foundation about the Bitcoin protocol and FOSS development to
the participants. With BDL, we want to identify talented programmers, improve
their Bitcoin protocol knowledge and skills, and provide the means to help them
turn into full-time open source contributors. The Bitcoin Dev Launchpad is built
upon the [Chaincode Labs'](https://learning.chaincode.com), [BTrust
Builders](https://www.btrust.tech/builders), and
[B4OS](https://www.libreriadesatoshi.com/b4os) programmes, adding to the global
educational Bitcoin landscape.

## Documents

This repo includes the documentation that details the program specifics and the
required infrastructure.

[Curriculum Structure](curriculum-structure.md)

### Phase 1: Extended Selection
[Mastering Bitcoin Seminar](https://github.com/vinteum-bdl/mastering-bitcoin-seminar)

### Phase 2: Main Cohort

### Infrastructure

## Tasks

The BDL program is a work in progress, we learn with every cohort and improve
for the next. These are open tasks for the second cohort.

- [ ] Move the
      [rpc-scanvenger-hunt](https://github.com/vinteumorg/task-rpc-scavenger-hunt)
      challenge as a warm up for those selected to the main cohort.
- [ ] Reestructure the program to include a Lightning Network track.
  - [ ] Write a HTLC programming challenge.
  - [ ] Write a Payment Routing programming challenge.
- [ ] Implement and test the autograder for the programming challenges. 
  - [ ] For the challenges with fixed expected data, check hash preimages
        instead of hardcoding the expected results.
  - [ ] Make the autograder automagically fill a spreadsheet so that we can
        focus solely on code review and minimize administration.
