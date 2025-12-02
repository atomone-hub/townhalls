# AtomOne Townhall Meeting 3 Notes

## Date: December 2nd, 2025, 10am PST

Link to the full transcript \[goes here\]  
Link to the full recording \[goes here\]  
Link to the full message log \[goes here\]

## Main Action Items:

* Join [AtomOne Rapture Club](https://t.me/youwillatone)
* Vote on existing chain proposal: [Prop 19](https://gov.atom.one/proposals/19)
* Sign up for newsletter on [Atom.One](https://atom.one/)

## Brief Summary of Discussion [goes here]

## AtomOne Chain Updates

* Activated PHOTON-only fees immediately, completing the fee side of the
  dual-token model before v3.  
    * [Prop 10](https://gov.atom.one/proposals/10)

* Signaling proposals for v3 features:
    * [Prop 9](https://gov.atom.one/proposals/9): Dynamic deposits will make it
      so proposal costs rise when governance activity spikes and fall when it
      cools. It will also burn proposals deposit if the percentage of no votes
      exceeds the set threshold (currently 80%).
    * [Prop 11](https://gov.atom.one/proposals/11): Added dynamic quorums that
      adjust governance turnout requirements to real participation.
    * [Prop 15](https://gov.atom.one/proposals/15): Dynamic fees à la EIP1559,
       with dynamic learning rate (additive increase, multiplicative decrease)
    * [Prop 14](https://gov.atom.one/proposals/14): Converted most ATONE in the
      Treasury and Community Pool into PHOTON.

* V3 upgrade (Nov 18th)
    * [Prop 18](https://gov.atom.one/proposals/18)

* Signaling proposal for v4 features:
    * [Prop 12](https://gov.atom.one/proposals/12): Signaled support for the
      Nakamoto Bonus to improve decentralization.

* Proposals in voting period:
    * [Prop 19](https://gov.atom.one/proposals/19): Fix the governance proposal
      deposit floor values.

* V4 features:
    * [Use a fork of the Cosmos-SDK](github.com/atomone-hub/cosmos-sdk)
    * [Upgrade to Cosmos-SDK v0.50](https://github.com/atomone-hub/atomone/pull/141)
    * [Nakamoto Bonus](https://github.com/atomone-hub/cosmos-sdk/pull/10)
    * [Fixed commission rate](https://github.com/atomone-hub/cosmos-sdk/pull/19)
    * [Governors](https://github.com/atomone-hub/atomone/pull/73)
    * [Core DAOs](https://github.com/atomone-hub/atomone/pull/188)

## IBC Update

The first GNOT transfer from Gno to AtomOne was completed a couple of days ago
between two local networks.

* Tendermint light client smart contract moved [here](https://github.com/allinbits/gno-realms)
* Tendermint2 light client [PR](https://github.com/atomone-hub/atomone/pull/232)
* TS-relayer compatible with IBCv2 [ibc-v2-ts-relayer](https://github.com/allinbits/ibc-v2-ts-relayer)

## Tooling and App updates

* Eclesia Indexer
  * v2 released.
  * Bug fixes
  * Performance and stability improvements
  * Boilerplating tool released (npx create-eclesia-indexer)
  * Enhanced testing and benchmarking suite

* Governance dApp 
  * Updated for v2 indexer
  * Bug fixes

* Staking portal
  * Bug fixes
  * UI improvements: Big thanks to @sherzod for contributing

## Delegation Program Updates
* Delegations were made
* Blog content to come
* UI improvements for delegation spread in progress

## Dither Updates

* [Added](https://github.com/allinbits/dither.chat/pull/468) support for account @handles
* [Proposed an implementation](https://github.com/allinbits/dither.chat/pull/494) to version prococol changes
* [Migrated to Bun Toolkit](https://github.com/allinbits/dither.chat/pull/480) from of pnpm & Node
* [Added](https://github.com/allinbits/dither.chat/pull/478) support for E2E tests w/ Keplr integration
* [Improved](https://github.com/allinbits/dither.chat/pull/436) frontend wallet integration
* UI improvements
* Security changes (Content Security Policy, enforce AUTH & JWT secrets)
* Quick demo of Dither account handle registration

## AtomOne Evangelists

* Feedback welcome on the [AtomOne Evangelists Program](https://docs.google.com/document/d/19JUazoOU7MQ04ZJBDybHpKHi914Us0XJdVEdc6CbU0U/edit?tab=t.0) 

## Open Discussion Time

* ### Advertising
*   We have started initial adversting trial campaigns on Reddit and Brave.
*   Shout out to the Cosmostation team running ads on Mintscan. 
<img width="2430" height="562" alt="image" src="https://github.com/user-attachments/assets/ac006660-d5b8-4c86-a89b-a0d191ca2364" />

* ### DAOs
- AtomOne Governance Hub, in the constitution it outlines the core daos and special purpose daos: Steering DAO and its subDAOs, Oversight DAOs and their subDAOs, Special Purpose DAOs and their subDAOs - starting with the BuidlDAO. What is the root DAO?
<img width="906" height="894" alt="image" src="https://github.com/user-attachments/assets/8d0b2f31-142a-45b2-8c6a-11e1f48a45bc" />


- Could this all be built out on Gno.land with the CommonDAO package?
- Once deployed on Gno.land and IBC is enabled, how would the treasury for BuidlDAO for example work, would it include GNOT, PHOTONS and ATONE?


* ### Outreach

* ### CMC Listing

* ### Upcoming CEX Listing?
