# REP-X: Community Conviction Score for Proof of Distribution

## Preamble

**REP:** X  
**Title:** Community Conviction Score for Proof of Distribution  
**Author:** Nova & Friends  
**Status:** Draft  
**Type:** Economic Incentive  
**Created:** 2026-06-02

---

## Abstract

This proposal introduces a Community Conviction Score (CCS) as a new component of Ronin's Proof of Distribution (PoD) framework. CCS allows RON holders to delegate support to builders and applications they believe create long-term value for the ecosystem. The score contributes a limited portion of a builder's overall PoD score and distributes a portion of builder rewards according to community conviction rather than solely activity-based metrics. The objective is to complement existing usage metrics with a measure of community commitment and builder-user alignment.

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/f3ee82fa-83a9-4cde-a0f4-d54be7daf929" />


---

## Rationale

Proof of Distribution rewards builders based on measurable ecosystem contributions such as user activity, retention, transactions, and economic value generated on Ronin.

While these metrics effectively measure ecosystem usage, they do not directly capture an equally important signal: community conviction.

Many projects cultivate highly engaged communities that actively support their long-term success. Community members often have stronger insight into a project's future potential than can be inferred from short-term activity metrics alone.

This proposal introduces a mechanism allowing RON holders to express conviction by delegating support behind builders. By allocating a limited portion of PoD rewards according to community conviction, Ronin can:

- Strengthen alignment between builders and users.
- Encourage long-term ecosystem participation.
- Increase utility and demand for RON.
- Provide an additional feedback signal beyond raw activity metrics.
- Enable RON holders to actively participate in ecosystem growth by supporting the builders they believe create long-term value.

Beyond its impact on reward distribution, Community Conviction Score introduces a unique ecosystem primitive for Ronin.

Most ecosystems reward builders through activity metrics, grants, or governance processes. Community Conviction enables users to directly support builders through RON delegation, creating a stronger relationship between token holders and ecosystem growth.

As a result, Ronin can become one of the first gaming ecosystems where communities actively participate in directing a portion of builder incentives toward the projects they believe are creating the most long-term value.

This strengthens alignment between builders, users, and RON holders while reinforcing Ronin's builder-first philosophy.

The proposal intentionally limits Community Conviction Score to a minority share of the Builder Score to ensure activity-based metrics remain the primary determinant of PoD rewards.

---

## Specification

### Overview

A new metric called Community Conviction Score (CCS) SHALL be introduced as a component of the Builder Score used within Proof of Distribution.

### User Delegation

Any RON holder MAY delegate support to one or more eligible builders.

Delegated support SHALL not transfer ownership of the underlying RON.

Delegated support MAY be modified or withdrawn by the user at any time, subject to protocol-defined cooldown periods.

### Builder Conviction Score

The exact methodology SHALL be determined by governance and may evolve over time.

Possible implementations include:

### Option A: Stake-Weighted Conviction

Builder CCS = Σ √(Delegated RON)

This approach rewards delegated support while reducing the influence of large individual stakeholders through square-root weighting.

### Option B: Composite Community Conviction Score

Builder CCS =
50% Stake Score +
25% Unique Supporter Score +
25% Long-Term Commitment Score

Where:

Stake Score:
- Based on total delegated RON.
- May use square-root weighting to reduce concentration.

Unique Supporter Score:
- Based on the number of distinct supporting wallets.
- Designed to reward broad community participation.

Long-Term Commitment Score:
- Based on average delegation duration.
- Designed to reward sustained conviction rather than short-term allocation.

This approach measures not only the amount of support received, but also the breadth and persistence of community engagement.

### Pilot Deployment

To minimize implementation risk and collect ecosystem feedback, this REP proposes an initial pilot deployment during the next Proof of Distribution season.

The pilot SHALL:

- Allocate 5% of Builder Score to Community Conviction Score.
- Run for a single PoD season.
- Collect participation and distribution data.
- Evaluate ecosystem impact before any permanent adoption.

Following the pilot period, governance MAY:

- Increase the weighting
- Maintain the existing weighting.
- Modify the scoring methodology.
- Discontinue the feature.

### Integration with PoD

For the pilot season, the final Builder Score SHALL be calculated as:

```
Builder Score =
95% Existing PoD Metrics +
5% Community Conviction Score
```

Following successful evaluation, governance MAY determine an appropriate long-term weighting for Community Conviction Score.

### Reward Distribution

Builder rewards allocated through PoD SHALL continue to be distributed according to the final Builder Score.

Builders receiving additional rewards through CCS MAY:

- Reinvest rewards into development.
- Fund community initiatives.
- Create ecosystem incentives.
- Reward players and users.

The protocol SHALL not impose restrictions on how builders utilize earned rewards.

### Builder Incentives

Builders MAY offer incentives to users who delegate support.

Examples include:

- NFTs
- In-game rewards
- Governance benefits
- Ecosystem tokens
- Exclusive access programs

Such incentives SHALL be managed independently by builders and SHALL not be enforced by the protocol.

### Builder Self-Delegation

Builders MAY delegate RON to themselves.

Given the limited weighting of CCS, self-delegation is considered an acceptable signal of commitment and ecosystem alignment.

Governance MAY introduce caps or alternative weighting mechanisms in future revisions if abuse emerges.

---

## Backward Compatibility

This proposal introduces no backward incompatibilities.

Existing Proof of Distribution calculations remain unchanged except for the addition of a new scoring component.

Applications that do not participate in Community Conviction Score continue to function normally within PoD.

---

## Security Analysis

### Whale Concentration

Large token holders may attempt to influence builder rankings through significant delegation.

This risk is mitigated by:

1. The limited contribution of CCS to the overall Builder Score.
2. The use of non-linear weighting functions such as square-root weighting.

As a result, delegation serves as a supplementary signal rather than a dominant ranking factor.

### Sybil Attacks

Because support is based on delegated capital rather than wallet count, Sybil attacks provide limited advantage.

Additional anti-sybil measures MAY be introduced if required.

### Reward Manipulation

Builders may incentivize delegation through rewards or promotional campaigns.

This behavior is considered acceptable and aligns with the objective of fostering stronger builder-community relationships.

Because CCS represents a minority share of the Builder Score, manipulation incentives remain limited.

### Governance Risk

Future governance decisions should monitor:

- Delegation concentration.
- Self-delegation levels.
- Incentive market behavior.
- Impact on PoD reward distribution.

---

## Economic Analysis

### Strengthened RON Utility

Community Conviction Score introduces an additional utility for RON beyond governance, and transaction fees. Users seeking to support builders and influence reward distribution must acquire and hold RON.

### Positive Ecosystem Feedback Loop

Users acquire RON

→ Delegate support to builders

→ Builders receive additional rewards

→ Builders invest in better games, applications or provide bigger reward pools

→ More users join Ronin

→ Greater ecosystem participation and network growth

### Increased Ecosystem Attractiveness

Community Conviction Score enables RON holders to become active contributors to ecosystem growth by supporting the builders they believe are creating long-term value.

This creates a stronger connection between builders, players, and token holders, aligning all three groups around the success of the ecosystem.

For builders, Community Conviction Score provides a new way to engage and grow their communities. For users, it provides a meaningful mechanism to support the projects they value most.

As a result, Ronin can become one of the few gaming ecosystems where communities directly participate in directing builder incentives, making the ecosystem more attractive to both builders and users and strengthening long-term network effects.

