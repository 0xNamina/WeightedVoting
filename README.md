# WeightedVoting

ERC-20 token with weighted voting system for decentralized governance and issue management.

## Description

This contract combines an ERC-20 token with a comprehensive voting system where voting power is weighted by token holdings. Users can claim tokens, create issues, and vote on proposals with their token balance determining their voting weight.

## Features

- **ERC-20 Token**: "WeightedVoting" (WV) with 0 decimals
- **Token Claims**: 100 tokens per claim, once per address
- **Issue Creation**: Token holders can create voting issues
- **Weighted Voting**: Voting power proportional to token balance
- **Quorum System**: Issues pass when quorum reached and FOR votes exceed AGAINST
- **Vote Types**: FOR, AGAINST, ABSTAIN

## Token Economics

- **Symbol**: WV (WeightedVoting)
- **Max Supply**: 1,000,000 tokens
- **Decimals**: 0 (whole numbers only)
- **Claim Amount**: 100 tokens per address
- **Voting Weight**: 1 token = 1 vote

## Voting Mechanism

1. **Create Issue**: Token holders propose issues with required quorum
2. **Cast Votes**: Users vote FOR, AGAINST, or ABSTAIN using their token balance
3. **Automatic Resolution**: Issues close when quorum reached
4. **Pass Criteria**: FOR votes must exceed AGAINST votes to pass

## Deployment Instructions

1. Open [Remix IDE](https://remix.ethereum.org/)
2. Create a new file and copy-paste the contract code
3. Compile the contract using Solidity ^0.8.0
4. Deploy on **Base Sepolia Testnet**
5. Interact with the functions:
   - `claim()` - Claim 100 voting tokens
   - `createIssue(string description, uint256 quorum)` - Create new issue
   - `vote(uint256 issueId, Vote voteType)` - Vote on issues
   - `getIssue(uint256 id)` - View issue details

## Vote Enum Values

- `0` = AGAINST
- `1` = FOR  
- `2` = ABSTAIN

## Submit Exercise

[📖 Submit ERC-20 Tokens Exercise](https://docs.base.org/learn/token-development/erc-20-token/erc-20-exercise)
