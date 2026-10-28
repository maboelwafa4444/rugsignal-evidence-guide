# A liquidity number answers a narrower question than “can I exit?”

Prepared21October2026 by RugSignal's maintainers; affiliated educational material, not an independent audit or trade recommendation. This note uses an explicitly illustrative example, not an investigation of a real pool.

A pool displaying $20,000 total liquidity does not necessarily offer $20,000 of the asset you want to receive. If a conventional two-sided pool held two sides valued at $10,000 each, adding them yields $20,000 TVL. It does not make the quote reserve $20,000. Concentrated and bin-based protocols add position and active-range considerations; this simple arithmetic does not model them.

Keep five questions separate:

1. Does the verified pool belong to the expected program and contain the exact mint?
2. What actual reserves, fee adjustments and pricing reserves were observed, and when?
3. Who or what currently holds withdrawal claims: fungible LP balances, positions or another documented mechanism?
4. What lock, burn or vesting evidence applies to those claims, including expiry and unresolved exposure?
5. What read-only route is available for the user's exact input quantity now?

A liquidity withdrawal can itself burn LP tokens. Therefore “LP burn happened” alone does not prove permanently surrendered claims. A small creator LP balance does not establish that other claims are locked. A successful quote is neither simulation nor execution and cannot guarantee future execution.

For a worked investigation, record the pool address, actual program owner, reserve units, withdrawal mechanism, claim-account references and observation time before writing a conclusion. If one is missing, say which question is unresolved. Do not convert absence into a Pass or accusation.

Primary protocol references: [Pump official AMM documentation](https://github.com/pump-fun/pump-public-docs), [Raydium protocol documentation](https://docs.raydium.io/), [Meteora documentation](https://docs.meteora.ag/). Their account layouts and operation semantics take precedence over a generic LP heuristic.

Use the [RugSignal liquidity guide](https://rugsignal.com/guides/liquidity-risk) and existing read-only exit assessment. If that guide URL changes, follow the [current guide index](https://rugsignal.com/guides). No swaps, wallet approvals or provider requests are initiated by reading this note. [Methodology and limitations](https://rugsignal.com/trust).
