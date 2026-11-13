# Monitor skill for Bankr

[Monitor](https://themonitor.bot), autonomous trading intelligence on Elysium (chain id 99901), driven from a Bankr wallet.

- `themonitor/SKILL.md` - what the agent does and the checks it runs before every signature
- `themonitor/catalog.json` - Bankr catalog entry
- `themonitor/scripts/verify-account.mjs` - checks on-chain that the smart account belongs to the user's wallet
- `themonitor/scripts/check-permission.mjs` - strict check of every permission before signing (pinned enforcers, exact terms, decoded limits)
- `themonitor/scripts/revoke.mjs` - revokes all permissions on chain from the user's own wallet

Funds stay in the user's own smart account. The wallet signs scoped, time-limited permissions (trade through the guarded contract only, withdraw to the user's wallet only, fee to the fee address only) and sends one deposit transfer.
