# AtomOne Townhall Meeting 1 Notes

##  Date: March 26th, 2025, 10am PDT

* [Link to the full transcript](https://docs.google.com/document/d/1B-uzMLu9ucw30R8D8WaQ_cHs8srqBAzKEQiLavfJcQE/edit?usp=sharing)
* [Link to the full recording](https://youtu.be/6Vg4xzaxM34)  
* [Link to the full message log](https://docs.google.com/document/d/1u3V8LXNCR3AVPMlDHzIEbWteRES1GjgrTtyJvx__MgE/edit?usp=sharing)

## Main Action Items:

* Join [AtomOne Community Discord](http://discord.gg/atomone)  
* [Vote](https://gov.atom.one/) on existing on chain proposal: PHOTON module and the Dynamic Deposit  
* Apply for [open roles](https://jobs.ashbyhq.com/allinbits)

## Brief Summary of Discussion: 

The call began with a welcoming of attendees and an outlining of the structure of the townhall. Participants were encouraged to contribute topics via GitHub and interact during Q&A sessions.

### Since Launch

* AtomOne chain has been live for 5 months and is steadily evolving\!  
* Airdropped to 1,128,299 Cosmos Hub (ATOM) addresses, accounts, with total ATONE genesis supply of 107,775,332 token  
* 5,388,766 ATONE were allocated to the Community Pool and 5,388,766 ATONE were allocated to a reserved address for the future funding of the AtomOne Treasury DAO  
* In the last 5 months, AtomOne has had an average of almost a 1,000 daily active accounts, and over 14x monthly users, just under a 117m circulating supply

### Covered proposals 1,2,3,4

* [Proposal 1](https://gov.atom.one/proposals/1) \- Enable IBC  
* [Proposal 2](https://gov.atom.one/proposals/2) \- Ratify Constitution  
* [Proposal 3](https://gov.atom.one/proposals/3) \- Logo Selection, Option \#1  
* [Proposal 4](https://gov.atom.one/proposals/4) \- Logo Selection, Option \#2

### Covered Current proposals 5 and 6 

* [Proposal 5](https://gov.atom.one/proposals/5) \- Signaling Photon Implementation  
* [Proposal 6](https://gov.atom.one/proposals/6) \- Signaling Dynamic Deposit mechanism, discussed a flaw in the dynamic deposit proposal
  * <details><summary>Current model flaw</summary>

    ![dynamic deposit flaw](/resources/townhall-01/dyn-deposit-flaw.png)

      - The time-dependent deposit increase actually incentivizes submitting proposals quickly rather than spacing them out. When deposits start increasing because `n_t` (the number of active proposals) exceeds the target `N`, rational actors would submit proposals as soon as possible before costs rise further
      - A sophisticated spammer could strategically time their attacks by bundling multiple proposals when deposits are low, then submitting them all at once. This would dramatically increase costs for legitimate users afterward but with no effect to the spammer which would only see cost between his submissions increase due to `n_t` changing (since they are bundled together roughly at the same time, or close in time)
      - The time-dependent increase mechanism disproportionately affects honest users who aren’t gaming the system, as they’re more likely to encounter elevated deposit requirements after spam attacks, because they aren’t timing their proposals wrt to network conditions, but more likely based on governance needs

    </details>
  * <details>
     <summary>Current vs new model</summary>

     ![dynamic deposit diagrams](/resources/townhall-01/dyn-deposit-cmp.png)

     - activation only increases, and time-based only decreases
    </details>
  * https://atomone-hub.github.io/govbox/depositv2.html
  * New proposal and updates to documentation and ADR coming: [PR](https://github.com/atomone-hub/atomone/pull/105)

### Covered Ongoing Engineering

* EIP-1559-like dynamic gas pricing \[[dev branch](https://github.com/atomone-hub/atomone/tree/feat/x/feemarket)\]
  * same module as Cosmos Hub now uses, removed proposer tip but [Additive Increase Multiplicative Decrease (AIMD)](https://github.com/atomone-hub/atomone/blob/feat/x/feemarket/x/feemarket/AIMD.md) implementation is indeed better than classical EIP-1559.
  * https://atomone-hub.github.io/govbox/feemarket.html
* Dynamic quorum: \[[dev branch](https://github.com/atomone-hub/atomone/tree/giunatale/gov/dynamic-quorum)\]  
  * Based on Tezos’s [dynamic quorum](https://octez.tezos.com/docs/active/voting.html#super-majority-and-quorum)  
* Governors \[[PR](https://github.com/atomone-hub/atomone/pull/73)\]  
  * [ADR](https://github.com/atomone-hub/atomone/blob/fabb95d83e9ddcbf6b0c237491020c12efc357a6/docs/architecture/adr-004-governors.md)

### Demonstrated the website, atom.one

* [https://atom.one/](https://atom.one/)  
  * We launched our first website describing the basic information about the chain, its features and the roadmap along with all the useful links and resources.  
  * We keep on working on the website, editing and polishing smaller parts. We welcome any feedback from the community and are determined to implement the necessary changes that arise with the growth of the chain.

### Centrifuge
An attendee demoed [**Centrifuge**](https://centrifuge.digital/), a Zealy/Galxe alternative for AtomOne:
  - Task platform with rewards, Discord roles, referrals.
  - Proposed for deployment on AtomOne to generate fee-based usage.
  - Live in beta; seeks community testing.

### Invited folks to the socials

* Discuss proposals on [Commonwealth](https://common.xyz/atomone)  
* Ask questions or troll around on [Discord](http://discord.gg/atomone)   
* Retweet/Repost on [X](http://x.com/_atomone)

### A Call to sign up the first community newsletter

* First community [newsletter](https://atom.one/#newsletter) releasing soon, sign up so you don’t miss the latest updates\!

### Covered the AiB ATONE Delegation Program 

* Details of [the AiB ATONE Delegation Program (Cycle I)](https://github.com/allinbits/AiB-ATONE-Delegation-Program)   
* Program Details: Application period: (January 8 \- Feb 4th)  
* Program Requirements:  
  * KYC verification for all applicants  
  * Public disclosure of conflicts of interest  
  * Validators with **over 3% voting power** ineligible to promote decentralization   
* Delegation Assessment and leveling criteria:   
  * Evaluation of contributions over the past month  
  * Ensuring a fair and transparent allocation of delegated tokens.  
  * Categorization into four levels based on past and future commitments:  
    * **Level 1 – Highly Engaged Contributors:**   
      * Provided technical contributions, integration tools, or services. Actively engaged in project development from inception.  
      * Participated in **Constitution workshops, GovGen working groups, and AtomOne Townhalls**.  
    * **Level 2 – Technical Contributors**  
      * Provided valid technical contributions.  
      * Did not previously participate in AtomOne or GovGen working groups.  
    * **Level 3 – Potential Future Contributors**  
      * Limited past contributions  
      * Plans for future contributions  
      * Provided concrete plans for future engagement in network growth.  
    * **Level 4 – Minimal Contribution**  
      * The validator has recently joined the AtomOne Community.  
      * No solid evidence of past contributions.  
      * No clear roadmap for future involvement beyond node operations.  
* ATONE Delegation Program (Cycle II) \> Application opens in August 2025  
* Ongoing evaluation of contributions and adherence to commitments throughout the next six months

* Concerns raised by an attendee over large, non-AIB delegations skewing decentralization.
* AiB confirmed plans to **redelegate away** from overpowered validators.


* Conversation steered into an explanation on how validator delegation no longer affects proposal votes. That delegators must vote directly; no inherited votes, and detailed future plans to improve delegation incentives before ICS rollout.

### Discussed DAO Structures and Laws

* Over the past few weeks, we’ve made substantial progress on the SteeringDAO Charter and the broader DAO governance framework.

* The initial version of the SteeringDAO Charter has been drafted to reflect its unique role as an advisory Core DAO. We’re currently working through the technical design of SteeringDAO’s on-chain actions. So too with the Oversight DAO. Very soon, we will seek community input to help fill the DAO council membership.

* Additionally, we’re revisiting the broader DAO governance framework after receiving community and contributor feedback. A constitutional amendment clarifying participation in Common DAOs is limited to Citizens may be necessary as the Constitution does not make it clear who can or cannot be a member of a Common DAO.

### Security, Audits and where people can find them

* Products contributed to by AiB engineering and their audit status:  
  * Staking dApp: Comprehensive audit (Zellic)  
  * Governance dApp  
    * Initial (GovGen) implementation : Comprehensive Audit  (Zellic)
    * AtomOne version: Differential audit for changes since previous audit (Zellic)
  * AtomOne daemon: Comprehensive Audit including proposed x/photon module and draft of dynamic deposit throttler (Zellic)
* [https://github.com/allinbits/security](https://github.com/allinbits/security)
* Launched Photon Community Bounty program: https://github.com/allinbits/grants/tree/main/Photon-Community-Bounty 

### Covered Chain activity stats, validators, network information

Attendee noted full validator set reached (100 max), open slots remain in lower-ranked validators, transaction volume and Nakamoto coefficient have improved.

* [https://www.mintscan.io/atomone/validators/](https://www.mintscan.io/atomone/validators/)

## Noted transactions since genesis

![Evolution of transactions since genesis](/resources/townhall-01/txs-since-genesis-1.png)

### Daily transactions

![Evolution of daily transactions since genesis](/resources/townhall-01/txs-since-genesis-2.png)

### Nakamoto evolution

The Nakamoto Coefficient was 4 three months ago, we are now at 7.

### Details on the staking.atom.one & gov.atom.one dApps

* [Staking Platform](https://staking.atom.one/)  
  * A one-stop dApp for staking ATONE and claiming rewards.	  
  * We launched the staking platform a few months back and we’ve been analyzing what community members have been talking about.  
  * We performed a security audit of the entire platform  
  * Based on community feedback and feedback from the audit we made UI/visual improvements to the platform.  
  * We’re looking into building alternative algorithms to help users stake to smaller validators, and give more options when choosing how to stake as well as further UI improvements.  
* [Governance Platform](https://gov.atom.one/)  
  * A dApp to allow for easy and effective participation in AtomOne governance.  
  * A comprehensive security audit was performed as well as a differential audit after the first few months of improvements and bug-fixes.  
  * We recently added some math formula code to the governance dApp which properly formats mathematical equations in markdown content.  
  * We’ve also been working behind the scenes on making performance improvements to the indexer and stabilizing it for public release at some point in the near future.  
* Both platforms have been added to the major dApps section of AtomOne on mintscan and support all major wallets (Keplr, Leap, Cosmostation)


### A mention of the new AtomOne docs

* A few members of the community were asking if we were going to launch documentation for AtomOne, and we can safely say we’vere launcheding it.  
* We’ve already put in the effort to aggregate documentation from the cosmos-sdk modules, and our own modules to create an open source documentation that anyone can contribute to.  
* Head on over to [https://github.com/atomone-hub/atomone-docs](https://github.com/atomone-hub/atomone-docs) if you want to contribute documentation, tutorials, or learn more about AtomOne.  
* Introducing [https://docs.atom.one/](https://docs.atom.one/)


Meeting wrapped up, a few calls to action:

 Vote on [Proposals 5 & 6](https://gov.atom.one/)
- Join discussions on [Commonwealth](https://common.xyz/atomone)
- Join the [Discord](http://discord.gg/atomone)
- [Sign up for the newsletter](https://atom.one/#newsletter)
- Apply for [open roles](https://jobs.ashbyhq.com/allinbits)

