# FaturaDev public documentation instructions

## Repository boundary

- This repository is the public Mintlify source for `https://fatura.dev`.
- Treat every tracked file, commit message, pull request, build log, and asset as `PUBLIC`.
- If material is not safe to publish without authentication, do not add it here.
- Keep internal architecture records, provider NDA material, operational runbooks, incident details, and agent transcripts in their approved private systems.

## Product language

- Use `FaturaDev` for the product and `fatura.dev` for the public site.
- Describe the product as a multi-provider e-Belge API and orchestration platform. The short category is “e-Belge Gateway”.
- State the operating boundary plainly: FaturaDev is not a GİB special integrator, does not connect directly to GİB, and does not perform financial-seal, electronic-signature, XAdES, or GİB-submission duties.
- Explain that those regulated transmission duties remain with the customer-authorized special integrator.
- Do not imply that a roadmap item, provider capability, API endpoint, or document type is generally available until its published contract says so.

## Public-safety rules

- Use only synthetic examples. Mark placeholders clearly and prefer `example.com`, non-production UUIDs, and deliberately non-valid identifiers.
- Never publish real VKN/TCKN values, names, addresses, invoices, XML/PDF artifacts, provider references, customer metadata, or production-like screenshots.
- Never publish passwords, tokens, API keys, certificates, cookies, authorization headers, private endpoints, internal hostnames, secret references, or encrypted secret values.
- Never publish NDA text, private provider documentation, copied partner portal content, vulnerability exploitation details, or raw production requests and responses.
- Do not paste raw agent transcripts or hidden prompts. Publish only reviewed, durable, public-safe documentation.

## Sources and verification

- Use primary sources for legislation, GİB packages, provider capabilities, standards, and API behavior.
- Link directly to the official GİB, provider, standards-body, or project page supporting the claim.
- Add a visible `Son doğrulama: YYYY-MM-DD` note to time-sensitive regulatory or provider documentation.
- If an official source is unavailable or ambiguous, label the point `Doğrulanmadı` and avoid presenting it as fact.
- Distinguish FaturaDev product decisions from external legal or provider claims.

## Mintlify content rules

- Every published page is an `.mdx` file with `title` and `description` frontmatter.
- Add every published page to `docs.json`; do not leave public orphan pages.
- Use root-relative links for repository pages and assets, such as `/quickstart` and `/images/brand/fatura-icon.png`.
- Keep headings in sentence case, use active voice, and explain one idea per sentence.
- Do not hand-author API operations that are absent from the published canonical OpenAPI artifact.
- Run `mint validate`, `mint broken-links --check-anchors --check-redirects`, and `mint a11y` before requesting review.

## Locked brand assets

- The only canonical brand files are `/images/brand/fatura-type.svg` and `/images/brand/fatura-icon.png` at the hashes recorded in `/images/brand/brand-assets.json`.
- Do not redraw, optimize, recolor, crop, rotate, animate, or silently replace these files.
- Do not invent a wordmark, icon, monogram, or logo variation.
- A brand change requires an explicit owner decision, a `brandVersion` increase, an updated manifest, and recorded output hashes.

## Contribution workflow

- Work on an issue-scoped `codex/<issue>-<slug>` branch.
- Never push directly to `main`, merge a pull request, publish a release, or deploy from an agent session.
- Keep each pull request focused and complete the public-safety and verification checklist.
