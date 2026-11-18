# yAudit Fellowship · Block 7 quizzes

Two Friday quizzes I picked and set for the fellows of the yAudit Fellowship, Block 7.
Each one is a contract to break: the answer is a working exploit.

## Quiz 1: The bridge

> A new bridge to another L2 has been deployed and someone just deposited a bunch of WETH...

A simplified L1/L2 ERC20 bridge derived from Optimism's standard bridge, with special handling for WETH.
**Goal:** drain the WETH held by the L1 bridge.

SafeBridge, a [Real World CTF 6th](https://github.com/iczc/rwctf-6th-safebridge) challenge (2024) by iczc, picked for this block.

Code: [`src/friday-quiz-1`](src/friday-quiz-1)

## Quiz 2: Magic of solidity

> Are you a solidity magician? Prove it.

**Goal:** make `Challenge.solve()` succeed. It deploys eleven `CrackMe` contracts with CREATE2 and calls each one under a gas cap; the results must combine into a magic number.

A Dreamhack challenge by [jinu.eth](https://twitter.com/lj1nu), built on [chainflag/solidity-ctf-template](https://github.com/chainflag/solidity-ctf-template), that I picked for this block.

Code: [`src/friday-quiz-2`](src/friday-quiz-2)

## Getting started

```bash
git clone --recursive https://github.com/fedebianu/yAudit-block-7-quizzes
cd yAudit-block-7-quizzes
forge build
```

Write your exploit as a Foundry test under `test/`.
