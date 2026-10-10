# SelectiCore v69 — Production Readiness

## Hardened in this build
- Cloudflare Pages Functions API
- Cloudflare D1 schema for users, sessions and progress
- Google ID-token verification against Google's JWKS
- HttpOnly + Secure + SameSite session cookies
- Session replacement on new sign-in
- Server-side progress storage with payload size guard
- Production security headers and CSP middleware
- Corrected cloud-restore precedence: cloud progress is authoritative when restoring
- Automatic cloud upload immediately after successful Google sign-in
- Guest/local mode retained
- Version metadata aligned to v69
- Local HTML asset/link audit and inline JavaScript syntax checks passed for this repair build
- 120 generated tests per subject passed the generator/quality gate without runtime errors
- 4,200 generated Maths questions and 4,800 generated Thinking questions were checked against independent formula/constraint validators with 0 mismatches in the audited templates
- Reading generator sample produced 17 groups / 38 answer parts with 38 unique stems per test; the static sample now has 100 passage-linked Reading questions
- See `QUESTION_BANK_AUDIT_REPORT.md` for the audit scope and limitations

## Required deployment configuration
Production cannot be activated without your own Cloudflare D1 database ID and Google OAuth Web Client ID. Those are deployment credentials/configuration, not hard-coded into the public package.

After configuration, deploy with Wrangler and run the D1 schema before accepting real users.
