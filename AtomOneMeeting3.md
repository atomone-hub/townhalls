# AtomOne Townhall Meeting 3 Notes

## Date: December 2nd, 2025, 10am PST

Link to the [full recording](https://drive.google.com/file/d/10S9F6BZ-1PHZK9TweA5T1H4tS2eQt4XB/view?usp=drive_web)  

Link to the [full transcript](https://docs.google.com/document/d/1n5gld5i3ENv3ilypt4pyTWNS8DNXcDks01o9s8wFk8c/edit?usp=drive_web)

Link to the [full message log](https://drive.google.com/file/d/1dP0WTuforzthcAqoEbtG_fnp7rZ6fd9W/view?usp=drive_web)

## Main Action Items:

* Join [AtomOne Rapture Club](https://t.me/youwillatone)
* Vote on existing chain proposal: [Prop 19](https://gov.atom.one/proposals/19)
* Sign up for newsletter on [Atom.One](https://atom.one/)

## Brief Summary of Discussion
In this town hall the AiB and community walked through recent AtomOne progress, upcoming v4 changes, cross chain work with Gno.land, tooling, delegation incentives, DAOs and outreach.

Engineers recapped v3 and the dual token model. PHOTON only fees were fully enabled and most ATONE in the treasury and community pool was converted to PHOTON. Governance parameters became dynamic. Deposits now rise when proposal load is high and fall when it is low, and quorums adjust toward the real participation level. Dynamic fees similar to EIP1559 were introduced with a learning rate that reacts to how far gas usage is from the target. The v3 upgrade went smoothly, but default deposit floors were accidentally left too low so Prop 19 was introduced to restore sensible minimums. Looking ahead to v4, AtomOne will run on its own fork of Cosmos SDK upgraded to v0.50, add the Nakamoto Bonus, enforce a fixed validator commission parameter starting at 5 percent, activate the Governors system for delegated governance voting, and wire in Core DAO logic so Steering, Oversight and Buidl DAOs can exercise the powers described in the constitution.

There were reports on IBC between Gno.land and AtomOne. Because Gno does not use Cosmos SDK, the team has been implementing IBC v2 style components. They already completed the first GNOT transfer from a Gno.land to AtomOne between local networks. This required a Tendermint light client smart contract written in Gno, an AtomOne light client for Tendermint2 headers, and a TypeScript relayer adapted for IBC v2.

Engineers also shared tooling updates. Eclesia indexer v2 was released with much higher throughput, better stability, boilerplate tooling and stronger tests and benchmarks. The governance app was updated to the new indexer and received bug fixes. The staking portal saw fee calculation fixes and UI improvements, including contributions from community member Sherzod. 

Dither received handle support, protocol versioning work, a migration to Bun, better wallet integration, new UI touches and security hardening through Content Security Policy and stricter auth and JWT handling. 

The AIB delegation program was presented, clarifying it is an AIB company program rather than a foundation program. The team is moving from infrequent large reallocations to more frequent smaller updates, potentially supported by a new UI and a multi stage scoring algorithm that considers uptime, missed blocks, infrastructure quality, relaying, marketing and other contributions. Validators NexuSecurus and Oneiric voiced strong views about commission levels, heavy selling, over reliance on cloud infrastructure and the need to reward validators who run their own hardware and invest in security. The group discussed publishing at least part of the scoring logic, building a public validator profile page that shows infra and contribution details, and possibly adding caps or non linear effects so top validators do not receive unbounded rewards, with some excess flowing to DAOs instead.

Representatives from Post Human presented a "quest and task platform" that could be migrated to AtomOne so that every quest and completion becomes an on chain transaction paid in PHOTON. The platform could host AtomOne bounties, "learn to earn" flows and user generated campaigns, potentially driving significant fee and IBC volume. He also previewed the Sputnik system that links user identities on services such as Twitter and Telegram to on chain addresses, which could inform the future Gno.land name system. Jae connected this work to the need for censorship resistant outreach and for rewarding people who create high quality educational and promotional content.

AiB contributors introduced the AtomOne Evangelists program concept, where a small cohort of community members would receive support and rewards to tell the AtomOne story in their own voices. There was also covered on initial advertising experiments that have started on Reddit and Brave, and Cosmostation was given a shoutout for running AtomOne ads on Mintscan. The group flagged the importance of better documentation for delegators, especially around the fact that validators do not vote on behalf of delegators on AtomOne and that Governors will soon change the governance experience again.

On DAOs, the call revisited the structure defined in the constitution for core and special purpose DAOs such as Steering, Oversight and Buidl. The group discussed using the CommonDAO package on Gno.land to prototype DAO behavior even before IBC is live, and then wiring treasuries that may eventually hold GNOT, PHOTON and ATONE. Jae suggested a public repository to collect nominations and background information for future Steering and Buidl DAO members and to log individual contributions that DAOs can later reward.

The call turned to open discussion with interest in collaboration from the Terra Classic community, general agreement that documentation and UX around delegation and governance should improve, and consensus that town halls should occur more frequently so contributors can stay up dated but still have time to build, propose and report back between sessions.

The call ended with a a demo on Dither handles and discussion on the need for a robust name system for Gno.land that avoids name squatting and can be reused across apps.

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

## Advertising
*   We have started initial adversting trial campaigns on Reddit and Brave.
*   Shout out to the Cosmostation team running ads on Mintscan. 
<img width="2430" height="562" alt="image" src="https://github.com/user-attachments/assets/ac006660-d5b8-4c86-a89b-a0d191ca2364" />

## DAOs
- AtomOne Governance Hub, in the constitution it outlines the core daos and special purpose daos: Steering DAO and its subDAOs, Oversight DAOs and their subDAOs, Special Purpose DAOs and their subDAOs - starting with the BuidlDAO. What is the root DAO?
<img width="906" height="894" alt="image" src="https://github.com/user-attachments/assets/8d0b2f31-142a-45b2-8c6a-11e1f48a45bc" />


- Could this all be built out on Gno.land with the CommonDAO package?
- Once deployed on Gno.land and IBC is enabled, how would the treasury for BuidlDAO for example work, would it include GNOT, PHOTONS and ATONE?

## Open Discussion Time

* ### CMC Listing

* ### DEX/CEX Outreach
