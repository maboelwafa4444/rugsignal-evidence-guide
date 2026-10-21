# A reproducible Solana token-risk checking worksheet

Use the same mint and approximately comparable observation times when comparing scanners. This worksheet describes a method, not a real investigation or accuracy result.

| Question | Evidence to record | Common interpretation error |
|---|---|---|
| What token is it? | Case-sensitive mint, program, decimals, source and observation time | Trusting a ticker or logo as identity |
| Which controls exist? | Current authority/extension account fields and applicable permissions | Treating a failed lookup as revocation |
| Who holds the supply? | Token accounts aggregated by owner, verified exclusions, supply denominator, completeness | Counting accounts as people or samples as exhaustive rankings |
| What connects wallets? | Actual transaction references, connection type and time window | Calling a shared service proof of common control |
| Which pool is assessed? | Pool address/program, lifecycle, selected market and freshness | Mixing price from one pool with volume from another |
| Who can withdraw? | Current LP/position claims, supported permissions, verified locks and release conditions | Treating TVL, zero creator balance or a quote as a lock |
| What exit size is quoted? | Human quantity, decimals, output, impact, fees, timestamp and route limits | Assuming future execution or subtracting included fees twice |
| What remains unknown? | Applicable unsupported/failed/stale domains and precise collection boundary | Converting missing evidence to Pass or to an accusation |

Illustration: one owner has two token accounts holding 3% and 2% of supply. The observed owner exposure is 5%, without renormalizing after pool exclusions. If the sample is incomplete, 5% is a lower bound; the accounts are not two independently verified people. A second graph path must not add the same holdings again.

Illustration: zero established warning points with 3/4 core domains verified does not resolve the fourth domain. Report the useful completed facts and the exact limitation together.

## Primary reading

- [Solana tokens and token accounts](https://solana.com/docs/tokens).
- [Authority configuration](https://solana.com/docs/tokens/basics/set-authority).
- [Token-2022 extensions](https://solana.com/docs/tokens/extensions).
- [RugSignal's sourced checking guide](https://rugsignal.com/guides/solana-token-risk-checks).
- [RugSignal methodology and limitations](https://rugsignal.com/trust).

Do not submit wallet secrets, personal customer information or confidential provider payloads when requesting a correction. Use the [on-site support form](https://rugsignal.com/support).
