# Elysium skill for Bankr

Copy-trading on Elysium (chain id 99901) through [elysium.dispatch.cash](https://elysium.dispatch.cash), driven from a Bankr wallet.

- `elysium/SKILL.md` - what the agent does and the checks it runs before every signature
- `elysium/catalog.json` - Bankr catalog entry
- `elysium/scripts/verify-account.mjs` - checks on-chain that the smart account belongs to the user's wallet

Funds stay in the user's own smart account. The wallet signs scoped, time-limited permissions (trade through the guarded contract only, withdraw to the user's wallet only, fee to the fee address only) and sends one deposit transfer.
