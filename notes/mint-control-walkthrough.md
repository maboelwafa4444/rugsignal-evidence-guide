# What a Solana mint-control check proves — and what it cannot

Prepared and observed 21 October 2026. Published by the RugSignal maintainers; this is an affiliated educational walkthrough. **Independent review pending. No predictive-accuracy claim.**

## Question and selection

Can two current mint accounts illustrate the difference between retained base authorities and revoked base authorities? We predeclared a convenience comparison of canonical USDC and the existing DUST Token-2022 benchmark before fetching either account. These two assets are not a random sample, outcome cohort or competitor benchmark.

One bounded `getMultipleAccounts` request returned both accounts at finalized context slot **459606480**, observed **2026-10-21T11:07:09.317Z**. One provider attempt took126ms; this is one request, not a general latency benchmark. The response's shared context applies to this batch, not all paginated collections.

| Base field | USDC | DUST |
|---|---|---|
| Mint | `EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v` | `5org5Hza3TQ3ps5LHYzQfZkJhokHF73AWc1vZZcmpump` |
| Program | Legacy SPL Token | Token-2022 |
| Decimals | 6 | 6 |
| Raw supply | `7360525019865623` | `971716688344686` |
| Base mint authority | Present | None |
| Base freeze authority | Present | None |

USDC mint authority: `BJE5MMbqXjVwjAF7oxwPYXnTXDyspzZyt4vwenNw5ruG`; freeze authority: `7dGbd2QZcCKcTndnHcTL8q7SMVXAkp688NTQYwrRCrar`. These are public controlling accounts, not inferred human identities. Supply is a raw account field, not market capitalization or proof of circulating supply.

## Reproduce the interpretation

1. Verify exact mint identity and the account owner, not the ticker. See [USDC account](https://solscan.io/token/EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v) and [DUST account](https://solscan.io/token/5org5Hza3TQ3ps5LHYzQfZkJhokHF73AWc1vZZcmpump). Explorers show current data, which may differ from this frozen observation.
2. Request base64 account data with `getMultipleAccounts` and explicit `finalized` commitment; retain the context slot and actual response time. A new request is a new observation, not reproduction of the old slot.
3. For the base mint layout, decode the mint-authority COption at bytes0–35, little-endian supply at36–43, decimals at44, initialized flag at45, and freeze-authority COption at46–81. Validate length, COption tags, program and initialization; never turn missing data into a revoked authority.
4. Compare those fields with the maintained parser. Our independent *code paths* agreed on ten fields using the **same** captured artifact. This is automated agreement, not independent source verification or independently reviewed factual accuracy.
5. For Token-2022, separately decode applicable extensions. This base-field exercise deliberately makes **no claim** about extension permissions, transfer fees, hooks, delegates, pause state or every possible restriction.

Frozen raw-artifact SHA256: `fbcd30d25b9572b316e660db7cff7630f3d6ce246d44fd310b81ed1b9e312623`. Raw provider payload is retained privately under the existing research policy; derived public facts are above. An independent reviewer needs the frozen artifact and must verify its origin, parsing and interpretation. A hash alone cannot prove provenance. Review has not occurred; no adverse outcome labels were assigned and predictive metrics remain unverified.

## Interpretation

An issuer retaining authorities on a reference stablecoin is a different assessment context from an ordinary memecoin. Revoked **base** authorities establish that those particular permissions were absent at the observation; they do not establish safe liquidity, independent holders, good project administration, future selling ability or investment quality.

Official contracts: [Solana mint accounts](https://solana.com/docs/tokens/basics/create-mint), [authority changes](https://solana.com/docs/tokens/basics/set-authority), [Token-2022 extensions](https://solana.com/docs/tokens/extensions), [getMultipleAccounts](https://solana.com/docs/rpc/http/getmultipleaccounts).

Next action: use the [RugSignal token-risk checklist](https://rugsignal.com/guides/solana-token-risk-checks?utm_source=github&utm_medium=referral&utm_campaign=evidence30) to investigate liquidity, holders and limitations separately. Campaign tags label this link; RugSignal's private coarse measurement does not claim campaign-level attribution. [Accuracy status](https://rugsignal.com/accuracy). Corrections should identify the exact field, timestamp and supporting evidence through [on-site support](https://rugsignal.com/support).
