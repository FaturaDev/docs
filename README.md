# FaturaDev documentation

This repository contains the public Mintlify source for [fatura.dev](https://fatura.dev).

FaturaDev is a multi-provider e-Belge API and orchestration platform. It gives software teams one integration surface for customer-authorized special integrator connections. FaturaDev is not a special integrator and does not connect directly to GİB or perform financial-seal, electronic-signature, XAdES, or GİB-submission duties.

## Published scope

The site is the public home for:

- product positioning and released capabilities,
- integration and usage guides,
- e-Belge and provider documentation backed by official sources,
- the versioned API reference after its canonical OpenAPI artifact is published,
- release notes and public operational notices,
- locked FaturaDev brand assets.

Internal architecture, credentials, real customer documents, personal data, provider NDA material, private endpoints, raw agent transcripts, and security-sensitive runbooks do not belong in this repository. See [AGENTS.md](./AGENTS.md) before editing content.

## Local development

Install the current [Mintlify CLI](https://www.mintlify.com/docs/cli):

```bash
npm install --global mint@latest
```

Start the local preview from the directory containing `docs.json`:

```bash
mint dev
```

The preview is available at `http://localhost:3000` by default.

## Validation

Run the same public documentation checks before requesting review:

```bash
mint validate
mint broken-links --check-anchors --check-redirects
mint a11y
```

Validate the locked brand files separately:

```bash
shasum -a 256 \
  images/brand/fatura-type.svg \
  images/brand/fatura-icon.png \
  images/brand/brand-assets.json
```

Expected values are documented on the [brand assets page](https://fatura.dev/project/brand-assets) and in `images/brand/brand-assets.json`.

## Contribution and publishing

1. Start from the current `main` branch.
2. Create an issue-scoped branch such as `codex/FD-123-short-description`.
3. Make public-safe changes and add every new page to `docs.json`.
4. Run the local validation commands.
5. Open a pull request and complete its public-safety checklist.
6. Obtain the required human and code-owner reviews.
7. Merge through the protected branch workflow. Do not push directly to `main`.

The Mintlify GitHub integration publishes reviewed changes from the configured production branch. Deployment credentials and private deployment procedures are not stored in this public repository.

## Brand assets

The canonical, immutable brand files live in [`images/brand`](./images/brand). Do not modify their bytes or create an alternative logo or wordmark. See [Marka varlıkları](https://fatura.dev/project/brand-assets) for hashes and usage rules.
