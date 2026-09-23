# Proof Hunters Agent Skills

Mine Hunter NFTs with an AI coding agent using the public [Proof Hunters CLI](https://github.com/vltgoblin/proof-hunter-miner). Mainnet is live on Robinhood Chain, chain ID **4663**.

## Install

From your agent's project directory:

```sh
npx skills add vltgoblin/proof-hunters-skills --skill proof-hunters-mining
```

Choose your agent when prompted, or add `--agent codex` or `--agent claude-code`. The installer defaults to project scope. Review the skill before installing. See the [Skills installer](https://github.com/vercel-labs/skills) for other supported agents. You can also copy the complete `skills/proof-hunters-mining` folder into your agent's supported skills directory.

## Start with a status check

Ask your agent:

> Use the proof-hunters-mining skill to check the live mainnet profile and mining status. Do not send transactions.

To mine, tell it which dedicated CLI wallet to use, the maximum gas cost per transaction in wei, the maximum number of calls, total gas budget, and CPU thread/attempt limits. Mining authorization includes an expired-seed refresh, which spends gas without minting an NFT. The skill asks for missing spending limits before proceeding.

The skill uses verified **v0.2.3** release bundles. It supports assigned HUNTER mining power and automatic expired-seed refresh. A fresh installation still needs the CLI, Python 3.9+, a dedicated encrypted wallet, and ETH for gas on the chosen network. Testnet source profiles are disabled; do not change them to bypass checks.

## What this provides

- Release verification and live network/profile checks.
- Bounded NFT mining calls, accurate result reporting, and pending-transaction recovery.
- Guidance for HUNTER power assigned to the exact CLI mining wallet.
- No private keys, wallets, or credentials in this repository.

This is an instruction package, not a hosted miner or a wallet sandbox. Installation does not grant spending permission. Your agent's tool permissions determine file and command access; keep wallet secrets out of its conversation. Mining produces NFTs, not liquid HUNTER tokens. Hardware and competition affect the chance of finding a proof; a run does not guarantee a mint.

[Skill](skills/proof-hunters-mining/SKILL.md) · [CLI releases](https://github.com/vltgoblin/proof-hunter-miner/releases) · [Setup guide](https://doc.proofhunter.fun/guides/cli/) · [Live deployment](https://app.proofhunter.fun/release.json) · [Website](https://proofhunter.fun)
