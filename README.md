# RugSignal — inspect the evidence behind a Solana token

[RugSignal](https://rugsignal.com/) is a Solana token-risk scanner for traders, researchers and developers. Basic scans need a mint address, not a connected wallet. Reports distinguish established findings, core-domain completeness and optional advanced investigations.

This is RugSignal's public educational and integration resource. It contains no application source, private SDK kit, API credentials or customer reports.

## Start with a question

- [Verify a mint and check token risks](https://rugsignal.com/guides/solana-token-risk-checks).
- [Understand mint and freeze authorities](https://rugsignal.com/guides/mint-freeze-authorities).
- [Investigate Pump.fun tokens and migration](https://rugsignal.com/guides/pump-fun-token-analysis).
- [Interpret holder concentration and wallet relationships](https://rugsignal.com/guides/holder-clusters).
- [Separate pool liquidity, withdrawal rights and exit quotes](https://rugsignal.com/guides/liquidity-risk).
- [Check Token-2022 restrictions](https://rugsignal.com/guides/token-2022-transfer-restrictions).

## Developer integration

The [public quickstart](https://rugsignal.com/developers/quickstart) explains the versioned Risk API, assessment fields, errors, freshness and signed events. The [OpenAPI specification](https://rugsignal.com/api/v1-openapi) is public. Live commercial access, credentials, private kits and sandbox onboarding require an [approved integration request](https://rugsignal.com/support?topic=integration); reading this repository grants no access or redistribution rights.

Stored-observation GETs do not initiate new scans. Preserve unknown states and observation times. Verify event signatures over the raw body and durably deduplicate event IDs. Never put a server API key in browser code.

## What a result means

Observed risk points are a weighted warning total, not a fraud probability or a universal score out of 100. A limited assessment with zero established points is not a safety guarantee. Core-domain completion and optional advanced coverage answer different questions.

Shared funding or a transfer does not prove common wallet ownership. A quote does not prove future sellability. A liquidity lock does not remove mint, holder or market risks. Independent predictive accuracy remains unverified. See the [methodology](https://rugsignal.com/trust) and [accuracy status](https://rugsignal.com/accuracy).

## Reading a report without confusing risk, coverage and price

Start with the exact mint and observation time. Read established warnings before treating the core-domain count as a verdict: a completed domain can contain a warning, and a limited zero-point assessment is not proof of safety. Open Coverage & Limitations to identify the unresolved domain, then investigate the corresponding holder or pool evidence. The [authority guide](https://rugsignal.com/guides/mint-freeze-authorities) includes a read-only checking sequence and a clearly illustrative revoked-mint/active-freeze example. The [liquidity guide](https://rugsignal.com/guides/liquidity-risk) distinguishes pool value, withdrawal rights, lock expiry and a size-specific exit quote.

The optional latest-price display is separate from the saved assessment. It polls a shared reference while actively viewed and may be delayed by provider freshness or quota limits. “Last fetched” is our successful source fetch, not the time of the last trade. It does not update holder balances, liquidity control, risk points or historical share cards. A displayed price or route quote is not a guaranteed executable sale.

For a reproducible factual example, the [mint-control walkthrough](notes/mint-control-walkthrough.md) includes its original observation time, slot, sources and limitations. It is an educational artifact awaiting independent review, not a predictive-accuracy benchmark. These materials are maintained on behalf of RugSignal; no independent endorsement is implied.

## Stay informed and report corrections

- [Product capabilities and limitations](https://rugsignal.com/ai-summary).
- [Guide updates, Atom feed](https://rugsignal.com/guides/feed.xml).
- [Evidence-checking worksheet](evidence-checklist.md).
- [Support and corrections](https://rugsignal.com/support).
- [Privacy](https://rugsignal.com/privacy).

Maintained by RugSignal. Educational information, not investment advice. No competitor superiority, partnership or endorsement is claimed. AI explanations may be unavailable; deterministic evidence remains separate. SOL/USDC subscriptions provide time-limited consumer access, not automatic API access or recurring wallet debit.
