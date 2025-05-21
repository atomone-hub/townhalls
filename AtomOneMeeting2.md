# AtomOne Townhall Meeting 2 Notes

##  Date: May 20th, 2025, 10am PDT

* Link to the [full transcript](https://docs.google.com/document/d/1CfEOa5Rjqw5BUUqRat4soLoN8s4gEIMGdpnIgqe0ZZU/edit?usp=sharing)
* Link to the [full recording](https://drive.google.com/file/d/1IPd1NH4kLZwMB_75eVr8tvfb1uqq_DVT/view?usp=sharing)
* Link to the [full message log](https://drive.google.com/file/d/1k1X460P7IJ04BAM2_kdLrX15vQv8oZKB/view?usp=sharing)

## Main Action Items:

* Join [AtomOne Community Discord](http://discord.gg/atomone)  
* [Vote](https://gov.atom.one/proposals/8) on existing on chain proposal: AtomOne V2 Upgrade
* Apply for [open roles](https://jobs.ashbyhq.com/allinbits)

## Brief Summary of Discussion: 

The second AtomOne Townhall opened with an overview of recent developments, particularly the AtomOne v2 upgrade proposal, which includes the introduction of PHOTON as a new fee token. The upgrade is scheduled for May 28, and validators were reminded to adjust their gas-prices accordingly. It was emphasized that PHOTON will not become the exclusive fee token immediately to allow time for ecosystem tools and commmunity to adapt.

The rest of the townhall essentially followed through the agenda as it is with some great presentations on ongoing engineering efforts, a "Nakamoto bonus" incentives structure for validators to increase Nakamoto coefficient and a sneak peak into some UI updates for staking.atom.one dApp.

### AtomOne Upgrade v2 proposal
* End of voting period: May 22th
* Halt-height is expected to be reached on May 28th.

### Roadmap & Ongoing Engineering
* V2 upgrade
  * https://www.mintscan.io/atomone/proposals/8
  * Introduction of the PHOTON token
  * Voting period end: May 22nd
  * Upgrade: May 28th (upgrade height: https://www.mintscan.io/atomone/block/3318000)
  * [Upgrading instructions](https://github.com/atomone-hub/atomone/blob/main/UPGRADING.md)
    * Validators will have to change their `gas-prices` setting.
* Signaling proposal for the new dynamic deposit
  * https://www.mintscan.io/atomone/proposals/9
* Tentative V3 roadmap (audit under negotiation)
  * Dynamic fee system (feemarket module)
    * https://github.com/atomone-hub/atomone/pull/114
  * Dynamic deposit
    * https://github.com/atomone-hub/atomone/pull/105
  * Dynamic quorum
    * https://github.com/atomone-hub/atomone/pull/135
  * Burn deposit if no votes > threshold
    * https://github.com/atomone-hub/atomone/pull/90
    * Threshold: 80%
* Govgen Sunset proposal
  * https://app.govgen.io/proposals/10
  * Scheduled for May 30th (halt height: 6900000)
* Nakamoto bonus
  * As a proof-of-concept, a presentation introduced the Nakamoto Bonus, a new incentivization mechanism designed to increase the Nakamoto Coefficient by encouraging delegation to lower-voting-power validators. The concept includes a dual reward model: proportional and constant per-validator. Feedback is encouraged. 
  * Find the presentation link here: https://docs.google.com/presentation/d/1G7bUJ_pJ7Ee3GYEvAtLZY1Z6Sf6YRp8E5cjbdgs8ryY/edit?usp=sharing

### Chain activity stats, validators, network information

* Chain stats showed relatively stable transaction volume and protocol fees, with some expectation noted for increased activity post-upgrade.

## Noted transactions (last 90 days)

![Evolution of transactions](/resources/townhall-02/txs.png)

## Protocol fees (since genesis)

![Protocol fees](/resources/townhall-02/protocol-fees.png)

### Nakamoto evolution

The Nakamoto Coefficient is 5.

### Docs
* Documentation updates were shared, including a redesigned validator services page and public RPC registry. A demo of the upcoming Staking dApp v2 followed, highlighting bulk stake and redelegation tools aimed at improving UX and decentralization.
* Documentation was updated to reflect the new AtomOne release versions.
* Re-organized some pages for better readability and navigation.
* 2 New Pages
  * [Services](https://docs.atom.one/validators/services.html) provides an overview of available validators and their security contacts.
  * [Registry](https://docs.atom.one/validators/registry.html) provides a list of RPC endpoints available to the public.

### Staking.atom.one & gov.atom.one
* Design updates included a preview of the Photon token logo with some discussion on the feature set of the new staking dApp features
* AtomOne Staking dApp v2 is a work in progress. At this stage AiB has a design for the new user interface that should cover most of the community’s requests along with some of our own ideas.

### Design
* AiB has a logo concept for the Photon token! You can find it on the [AtomOne Hub repo](https://github.com/atomone-hub/assets/blob/main/logos/PNG/photon-token-round.png) 

### Socials

* Review and provide feedback on upcoming proposals on [Commonwealth](https://common.xyz/atomone)  
* Discuss with the community on [Discord](http://discord.gg/atomone)   
* Retweet/Repost on [X](http://x.com/_atomone)

### Newsletter

* The first AiB AtomOne newsletter released last week. Sign up now for progress updates in the next [newsletter](https://atom.one/#newsletter)

### Keplr Integration
* ATONE has officially been [integrated in Keplr wallet](https://x.com/keplrwallet/status/1922978693065974206) along with the AtomOne testnet in the [Keplr chain registry](https://chains.keplr.app/)

Finally, a full-feature explorer was shared by Nodeist at https://atomone.ist/

### Grants

* Review and provide feedback on grant proposal. Join the discussion and share your thoughts. [📝 Grants Request on Commonwealth](https://common.xyz/atomone/discussion/1259471-grant-proposal-atomoneist-fullfeature-explorer-for-atomone-mainnet-testnet)

The meeting closed with a brief discussion about the validator-as-a-service topic (with no significant update yet) and appreciation for those joining.
