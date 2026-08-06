# USAspending.gov API Reference

Live at: **https://conorscode.github.io/usaspending-api-reference/**

A verified reference for USAspending.gov's public `spending_by_award` search API, documenting two undocumented behaviors we hit building a production scraper against it:

1. The `fields` array is not server-validated — unknown field names silently return `null` instead of erroring.
2. `page_metadata.hasNext` is unreliable past roughly page 100 of a large sorted query — it reports `false` while further pages keep returning full rows.

Also covers the 50,000-row simple-pagination cap and cursor workaround, the 100-row `limit` cap, money-field semantics (obligated vs. outlays vs. ceiling), and the award type codes reference.

Every claim on the page was re-verified against the live API on 2026-08-05.

MIT licensed — see [LICENSE](LICENSE).
