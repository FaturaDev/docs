# FaturaDev public documentation instructions

## Repository boundary

- This repository is the public Mintlify source for `https://fatura.dev`.
- Treat every tracked file, commit message, pull request, build log, and asset as `PUBLIC`.
- If material is not safe to publish without authentication, do not add it here.
- Keep internal architecture records, provider NDA material, operational runbooks, incident details, and agent transcripts in their approved private systems.

## Absolute public publication boundary

`fatura.dev` is a marketing, product, integration and API documentation site for anonymous visitors, prospects, customers and external developers. It is **not** an internal wiki, decision journal, project tracker, provider-readiness notebook or agent workspace.

Before adding any tracked content, answer both questions:

1. Which anonymous public audience needs this information?
2. What concrete public product or integration benefit does it provide?

If either answer is missing, do not add the material to this repository or its Git history.

Never publish or copy:

- conversations between the owner, team members or agents,
- agent session/handoff notes, prompts, tool output or task status,
- internal ADR/RFC discussions, spikes, research notes, decision rationale or issue/PR planning,
- repository governance, purchasing, staffing, credentials or deployment/operation procedures,
- provider sales discussions, partner onboarding, private sandbox provisioning, commercial terms or written-confirmation questions,
- unpublished provider order, roadmap, release target, benchmark, architecture topology or implementation dependency,
- private repository, issue, pull-request, local filesystem or access-controlled evidence links,
- a capability, endpoint, quota or workflow that is not present in the published customer contract.

`.mintignore`, an orphan `.mdx` page, an unlinked asset or a draft filename does not make tracked content private. Team-only drafts must remain outside this repository.

When publication safety or product availability is uncertain, set the outcome to `PUBLICATION_BLOCKED`: make no content change, keep the source in the approved private system and request an explicit public-safe version. Silence is safer than publishing internal context.

## Locked Tahsil design

The public documentation design is a 1:1 FaturaDev adaptation of [`muhasip/tahsil`](https://github.com/muhasip/tahsil) at commit `a86e7650bc0a5a24fbf384679ab60db853d0dd5f`.

- Keep the Mintlify `almond` theme, neutral color palette, appearance, interaction and styling settings identical to that reference.
- Keep the reference `custom.css` byte-for-byte: CTA styling and centered navigation tabs must not drift.
- Follow the same language → tabs → groups navigation hierarchy and the same homepage section/CardGroup composition.
- Do not invent another theme, color, font, component, layout, CSS rule, animation or visual pattern.
- Substitute only FaturaDev's locked brand assets, public product copy, public routes, domain, GitHub link and genuinely published API contract.
- Never copy Tahsil product text, API operations, credentials, production endpoints, analytics, customer data or Tahsil brand assets.
- If Tahsil contains a feature that FaturaDev has not publicly released, omit the page or control; do not fabricate a placeholder contract.

A design change requires the owner's explicit decision, a newly pinned Tahsil reference when applicable, updated policy checks and a focused pull request. Ordinary content work cannot change the locked design.

## Locked Twenty information architecture

The public landing and documentation structure follows
[`twentyhq/twenty/packages/twenty-docs`](https://github.com/twentyhq/twenty/tree/c503d4c4aaa29c978d8c190ad8232658e970d06c/packages/twenty-docs)
at commit `c503d4c4aaa29c978d8c190ad8232658e970d06c`.

- Keep three public top-level documentation surfaces: `Başlangıç`, `Ürün Rehberi`, and `Geliştiriciler`.
- Keep the landing flow positioning-first: a concise product statement, differentiators, audience fit, non-fit, and a clear next step.
- Use overview pages as section entry points. Add `Referans` and `Nasıl yapılır?` groups only for capabilities that are already released and supported by public product contracts.
- Keep API, webhook, OAuth, provider, self-hosting, or contribution groups absent until each subject has a genuinely published FaturaDev contract or public program.
- Adapt the hierarchy and content rhythm only. Never copy Twenty product claims, prose, screenshots, illustrations, brand assets, source code, or unreleased FaturaDev promises.
- The Twenty information architecture does not override the locked Tahsil visual system. Do not copy Twenty CSS, imagery, components, card art, or layout styling.

Changing the three top-level surfaces or the positioning-first landing flow requires
the owner's explicit decision, an updated pinned reference, policy checks, and a
focused pull request.

## Product language

- Use `FaturaDev` for the product and `fatura.dev` for the public site.
- Describe the product as a multi-provider e-Belge API and orchestration platform. The short category is “e-Belge Gateway”.
- State the operating boundary plainly: FaturaDev is not a GİB special integrator, does not connect directly to GİB, and does not perform financial-seal, electronic-signature, XAdES, or GİB-submission duties.
- Explain that those regulated transmission duties remain with the customer-authorized special integrator.
- Do not imply that a roadmap item, provider capability, API endpoint, or document type is generally available until its published contract says so.
- Do not name a planned provider or publish provider order until that integration is publicly announced and documented.

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
- Every tracked `.mdx` page must be present in `docs.json`; hidden or orphan content is forbidden.
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
