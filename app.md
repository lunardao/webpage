
**LunarDAO architecture is based on [Moloch V3](https://github.com/Moloch-Mystics/Baal) design, ran by [DAOhaus](https://daohaus.club/moloch) and customized to fit LunarDAO [governance](https://github.com/lunardao/dao).**

<!---BUTTONS:--->

[JOIN](https://join.lunardao.net) [DAO](https://admin.daohaus.fun/#/molochv3/0x1/0x747da68facd1459e9d9b8f928418da30769d3ba1)


## How to Join

- It is recommended to [anonymize your assets](https://wiki.lunardao.net/anonymizing_assets.html) before joining the DAO.
- Go to [The Staking page](https://join.lunardao.net). The entry is permissionless, but only opened between **April 16th, 17:00 UTC and April 30th, 17:00 UTC**.
- **$VOX** represent the members share of the treasury as well as their voting power (voting power can be delegated as well).
- $VOX (shares) are non-transferable.
- Everyone's entry price is the same: 1 ETH = 100 $VOX (- fees).
- The minimum tribute in order to join the DAO as a Squad member is 0.1 ETH which equals 10 $VOX (shares).  
- Admin/management fee on entry of 0.25% is paid to the [Stewards' (core-team) account](https://app.safe.global/home?safe=eth:0xAb501a8Eb58c9780eb04D683feB504fcE391A2DD) from every tribute in the form of $VOX for the [DAO operations](https://github.com/lunardao/dao#stewards).

## Governance TL;DR

Read LunarDAO [Manifesto](https://wiki.lunardao.net) and the [whitepaper](https://github.com/lunardao/dao) to know more about LunarDAO: [Mission](https://github.com/lunardao/dao#mission), [Governance](https://github.com/lunardao/dao#governance) and [DAO architecture](https://github.com/lunardao/dao#lunardao-architecture). To learn about the plans, check out the [Roadmap](https://lunardao.net/roadmap.html). 

This is the initial governance setup for LunarDAO governance (changes can be [proposed](https://admin.daohaus.fun/#/molochv3/0x1/0x747da68facd1459e9d9b8f928418da30769d3ba1/proposals) any time):

- **LIP (LunarDAO Improvement Proposal):** A proposal is created and shared with the community. Use the template in [LIP-0001](https://github.com/lunardao/lip/blob/main/lip-0001.md).  
- **Forum discussions:** A thread is created on the [forum](https://forum.lunardao.net/c/proposals), where the LIP is discussed. The proposal should be announced at least 7 days before voting.
- **Voting:** A proposal is submitted on-chain and the voting is opened for 72h.
- **Grace Period:** Follows voting for another 72h. Members can exit the DAO with their funds if they don't want to be affected by the decision.  
- **Execution:** Proposals are submitted on chain, hence the changes will apply automatically with pushing the execution button.   
    - If treasury unrelated: Stewards update the documents.

## Contracts

LunarDAO Treasury: [0x59F77dC848C2E45B5954975ee1969e7A22fA25F6](https://app.safe.global/settings/setup?safe=eth:0x59f77dc848c2e45b5954975ee1969e7a22fa25f6)\
Moloch V3 DAO (LunarDAO Governance): [0x747DA68Facd1459E9D9b8f928418DA30769D3Ba1](https://etherscan.io/address/0x747DA68Facd1459E9D9b8f928418DA30769D3Ba1)\
Sentinels' Safe (5/8 multi-sig): [0x622066aBA170c185c28cED6E7ccd1cB2047ef6ef](https://app.safe.global/home?safe=eth:0x622066aBA170c185c28cED6E7ccd1cB2047ef6ef)\
LunarDAO Stewards' Safe (core-team, founders): [0xAb501a8Eb58c9780eb04D683feB504fcE391A2DD](https://app.safe.global/home?safe=eth:0xAb501a8Eb58c9780eb04D683feB504fcE391A2DD)\
$VOX (voting token/treasury shares): [0x33e6ded5073f512475e17b5f19dda90d9a782478](https://etherscan.io/address/0x33e6ded5073f512475e17b5f19dda90d9a782478)\
$VOX-LOOT (non-voting token/shares): [0x94fadf770e44b7bc872fc712e4ba6aaf096fcba7](https://etherscan.io/address/0x94fadf770e44b7bc872fc712e4ba6aaf096fcba7)\

## Veto Agent

LunarDAO deployed a [Sentinel committe](https://github.com/lunardao/dao#sentinels) (a [multi-sig safe](https://app.safe.global/home?safe=eth:0x622066aBA170c185c28cED6E7ccd1cB2047ef6ef))  as a veto agent. At the same time the DAO architecture itself is based on [Moloch V3 primitive](https://github.com/lunardao/dao#moloch-v3) with a full on-chain execution. This contradiction is solved by a design where the main [LunarDAO treasury](https://app.safe.global/settings/setup?safe=eth:0x59f77dc848c2e45b5954975ee1969e7a22fa25f6) is a Gnosis Safe with two signers of which only one is needed for an execution (1/2). The two signers are:

1. [LunarDAO Squad](https://github.com/lunardao/dao#squad): a [Moloch V3 DAO](https://github.com/lunardao/dao#moloch-v3), [Contract](https://etherscan.io/address/0x747DA68Facd1459E9D9b8f928418DA30769D3Ba1)
2. [LunarDAO Sentinels](https://github.com/lunardao/dao#sentinels): [Gnosis safe (5/8) multi-sig](https://app.safe.global/home?safe=eth:0x622066aBA170c185c28cED6E7ccd1cB2047ef6ef)

In this setup all the proposals are submitted, voted upon and (after grace period) executed on-chain without any Sentinel interaction. Only in the case of a [malicious proposal](https://github.com/lunardao/dao#sentinels), the Sentinels can step in and reject the proposal. Five Sentinel members must sign a veto in their [safe](https://app.safe.global/home?safe=eth:0x622066aBA170c185c28cED6E7ccd1cB2047ef6ef) in order to make such execution in the LunarDAO treasury. 

![](https://github.com/lunardao/dao/raw/master/pic/diagram_treasury.png)
