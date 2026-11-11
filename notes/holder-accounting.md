# Token accounts, owners and people are different denominators

Prepared21October2026 by RugSignal's maintainers; affiliated educational material. All numbers below are illustrative, not real wallet findings.

Suppose an owner holds60 tokens in one account and40 in another while a pool vault holds100. Ranking raw token accounts differs from aggregating balances by their actual token owner. Neither count establishes the number of people or common beneficial control.

For an interpretable concentration metric, record:

- Exact mint, token program and compatible supply observation.
- Token-account collection source, interval, pagination exhaustion and caps.
- Deduplication and integer balance arithmetic before owner aggregation.
- Independently verified pool/service exclusions and why they apply.
- Ranking after aggregation and exclusions; percentages still use the original compatible supply denominator.
- Whether top-N owners are complete or only observed lower bounds.

Solana's largest-account RPC returns at most20 token accounts. That alone cannot prove a complete top-owner ranking: an owner may have other accounts outside the sample. A partial lower bound may establish a high-concentration condition, but a low partial result cannot prove low total concentration.

A supported funding transfer establishes a relationship of that type. It does not automatically establish common ownership, coordinated buying or selling. Deduplicate overlapping groups before summing exposure; never add the same wallet's balance twice. Common exchange funding and router use require particularly careful interpretation.

Primary sources: [Solana getTokenLargestAccounts](https://solana.com/docs/rpc/http/gettokenlargestaccounts), [Helius holder enumeration](https://www.helius.dev/blog/how-to-get-token-holders-on-solana). Paginated reads are not automatically an atomic historical snapshot.

Apply this checklist to the [RugSignal holder guide](https://rugsignal.com/guides/holder-clusters) and inspect the saved report's holder and relationship evidence. [Methodology](https://rugsignal.com/trust) and [support/corrections](https://rugsignal.com/support). None of these metrics alone proves insider identity or predictive accuracy.
