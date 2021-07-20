# A Decentralized Model for Land Ownership and Management


## Contents 

1. Introduction
1. Motivation
1. Previous attempts
1. Philosophy
1. Governance
1. Technical implementation
1. Applications
1. References

### Introduction

When Bitcoin launched in 2009, Satoshi proved that value could be stored and transmitted securely without intermediaries. The subsequent release of Ethereum proved that a Turing complete, distributed computer meant that arbitrary state and computation could be put on chain, enabling smart contracts that define complex relationships and agreements between people. 

The impact and reach of blockchain technology is largely confined to the digital sphere. Some novel experiments like [Unisocks](https://unisocks.exchange/) have tokenized real world assets, in this case giving owners a physical pair of socks in exchange for burning a SOCKS token. Unfortunately, the exchange of real-world assets usually relies on centralized trustees - in this case the Uniswap employee sending socks when a token is burned. A rogue sock distributor could simply not send the socks, and the blockchain would never know.

Perhaps socks will never be fully on chain, but fortunately ownership of real estate is a matter of deed.  Deeds are documents that can be held by LLCs, individuals and banks.

Wyoming's [DAO Law](https://www.wyoleg.gov/2021/Introduced/SF0038.pdf) opens the door to forming LLC entities and recognizing the rights and decisions of members as legally binding decisions that will be recognized in a court of law:

> Management of a decentralized autonomous organization shall be vested in its members, if member managed, or the smart contract, if algorithmically managed, unless otherwise provided in the articles of organization or operating agreement (p. 11)

Since LLCs can hold real estate deeds, this means a DAO can hold, manage, and make decisions regarding land owned.

### Motivation

Digitizing physical assets can increase accessibility, improve liquidity, and bring interoperability.

As a case study, compare the difference between converting \$100 to EUR and converting $100 ETH to USDC. The blockchain-native, digital conversion is instant, accessible, transparent, and has lower fees.

Currently, real estate is largely offline and transactions require intermediaries, large sums of capital, and extensive legal paperwork. What Satoshi and Buterin did for value and compute, we propose to do for real estate.

### Previous Examples

Like DAOs themselves, various forms of tokenized real estate transactions have been [a dream of members of the Ethereum community since it’s earliest days](https://blog.slock.it/decentralized-sharing-economy-to-be-revealed-at-leading-blockchain-conference-f419f15beb7f?gi=828f6c1a9ee1).  [Countries have worked to put title registries on chain](https://ethereumworldnews.com/uaes-capital-abu-dhabi-to-place-land-registry-on-blockchain-based-platform/), [several teams](https://medium.com/meridio/meridio-the-new-standard-for-shared-ownership-of-physical-assets-ce6291050a38) [have tried putting traditional LP units of real estate syndications on chain](https://www.coindesk.com/harbor-tokenizes-real-estate-funds-worth-100-million-on-ethereum), and none of these efforts have really achieved product market fit.

### Philosophy

Coming soon....
### Governance

All decisions regarding land acquisition, use, rights, and policies will be decided by CityDAO. By purchasing land through the DAO, purchasers agree to follow the collective policies set by the DAO on land use, taxation, and rights.

The CityDAO governance token will be an ERC-20 token. Holders will vote on proposals that will pass with a 50% + 1 vote majority and the DAO itself may change hyperparameters like vote quorum thresholds and vote delegation rules.

**Smart contracts as legal documents**

Wyoming's DAO law gives legal recongition to the underlying claims of the smart contract, so the general powers of CityDAO are large in scope and only confined to the law of Wyoming and the USA. 

**Powers of the members of CityDAO**

The most primitive way to link physical objects to on chain ones is to rely on a trusted third party. For example, a deed to land or a house is tokenized and held by a trustee who signs a binding agreement to execute actions that a smart contract dictates. Much like Unisocks, this is vulnerable to a malicious trustee, who could steal the deed to the house.

Using Wyoming's new DAO law, however, using trustees is more feasible because there is legal recourse and recognition of the DAO LLC. Since the actions of the DAO LLC have legal standing in Wyoming, this would violate the law, the DAO could recover the land. For interfacing with some institutions, the DAO shall assign trustees who take actions on behalf of members. 

CityDAO may make any proposal that is congruent with Wyoming and US law, but here are some common responsiblities of the DAO:
- LAND MANAGEMENT: Purchasing new land, developing and/or using land, and selling land.
- CONFLICT RESOLUTION: Resolving conflicts between parties, for example boundaries, natural resources, and conflicts of land use.
- TAXATION: Setting tax on land ownership or transfer. 
- TRUSTEE DESIGNATION The intention of the project is to minimize interactions with non-digitally native institutions like banks, notaries, and county assessors, but we acknowledge that it may be be needed, for which we propose the DAO elect a Trustee. 

Since smart contracts may be amended, CityDAO members may vote to grant members additional powers.

**Trustee designation**

For interfacing with some institutions, the DAO shall assign trustees who take actions on behalf of members. Smart contracts will implement an `electTrustee` method who will be authorized to take an action with a purpose. Note, the trustee need not be a member of the DAO.

### Technical implementation

Land parcels will be ERC-721 tokens (also known as NFTs). Initial parcels will be collectively owned by the DAO, but some parcels may be sold to individuals in the DAO or externally.  

Parcels may be fractionally owned by issuing an ERC-20 governance token over that specific parcel.

Pursuant to the discussion on Powers of CityDAO, the governance contract shall implement the followng methods:

- join
- fund
- createProposal
- voteOnProposal
- assignTrustee
- openDispute
- setAnnualTaxRate
- setYearlyTaxRate

[in discussion]

## Land Use

The DAO may choose to hold land or use land with a vote. An example of the governance process. CityDAO votes to acquire a parcel of land proposed by Member A. CityDAO members vote to build a wind energy farm, and assign a Trustee to implement the use case.

**Community campground**
A campground can be established which members of the DAO may use freely. Communal ammenities could be funded through votes of the DAO.

**NFT parcels**
The DAO may designate a land area as individual plots and sell them to individuals.

**Bitcoin Mining**
Buy or Rent a warehouse. Buy ASICs. Make agreement with local utility to use wind energy. 

**Hunting/Fishing Resort**
Buy land along a river. Provide exclusive hunting and fishing access. (ie. elk hunting, flyfishing) Will need to hire someone to maintain the business.

**Land or camping rentals**
Use HipCamp or Airbnb to provide access to the property.

**Farming**
Buy land and make agreement with a local farmer. Note: This would require a member of the DAO to speak with farmer to make the agreement every season. The profit margins for the DAO would be low and seasonal.

**Housing**
Buy an apartment building. Hire a management company to collect rent and do repairs.
## Annotated Bibliography

1. Wyoming DAO Law full text - https://www.wyoleg.gov/2021/Introduced/SF0038.pdf
1. RealT whitepaper - https://realt.co/wp-content/uploads/2019/05/RealToken_White_Paper_US_v03.pdf
