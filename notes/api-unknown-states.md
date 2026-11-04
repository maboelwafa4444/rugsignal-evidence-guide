# Integrating a risk report without turning “unknown” into “safe”

Prepared21October2026 by RugSignal's maintainers. Affiliated developer education; live commercial access requires operator approval and provider rights. No credentials are issued by this document.

An integration needs at least three independent concepts: established findings, applicable core-domain completeness, and optional advanced-analysis status. Freshness and asset/model applicability belong alongside them. A returned HTTP200 report is not proof that every domain completed.

A useful presentation contract preserves numeric zero, missing values and inapplicability separately. This language-independent example is illustrative presentation logic, not a promise of field names in every API version:

```
if model is inapplicable: explain why it is not scored
else if points is a finite number: display observed risk points, including 0
else: explain why no defensible numeric result exists
always display applicable domain limitations and consequential established warnings
```

Do not use `if (points)` to distinguish zero from absence. Do not default an absent number to0, renormalize failed checks into passes, or label a partial0 as “safe.” A serious verified warning remains important even when another provider times out.

For example, a purely illustrative report with0 observed warning points and3/4 verified core domains can say that no warning points were established in completed checks while naming the unresolved liquidity domain. That is not a calibrated fraud probability or complete safety verdict.

Use the current [public quickstart](https://rugsignal.com/developers/quickstart), [OpenAPI contract](https://rugsignal.com/api/v1-openapi) and [integration request](https://rugsignal.com/developers) rather than copying private operational examples. Preserve unknown states, source time, applicability and documented errors in downstream caches. Verify signed events using the published contract; do not place partner secrets in browser code.

[Solana commitment reference](https://solana.com/docs/rpc) explains why observation context matters. [RugSignal accuracy status](https://rugsignal.com/accuracy) separates software behavior from independently established predictive performance.
