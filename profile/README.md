# EUDI Wallet Verifier Kit

Framework-agnostic verifier kit for the European Digital Identity Wallet.

`eudi-verify` provides a drop-in web component, typed client SDK, React wrapper, Node.js server handlers, and an OpenAPI specification for websites that want to experiment with EUDI Wallet-style verification flows.

## What is this?

**[eudi-verify](https://github.com/eudi-verify/eudi-verify)** helps websites and services integrate EUDI Wallet credential verification quickly.

Think of `eudi-verify` as a reCAPTCHA-style integration pattern for credential verification: a small embeddable widget starts a wallet verification flow and returns a server-verifiable token, enabling age checks, credential proofs, and scoped identity attributes without building the full protocol stack.

```html
<!-- Add age verification to any website -->
<eudi-verify api-url="/api/eudi" request='{"age_over_18": true}'></eudi-verify>
```

**Live demo:** https://demo.eudi-verify.eu/

Use cases include proving a user is over 18, verifying possession of a specific credential or entitlement, and checking a scoped identity attribute without building the full verifier flow from scratch.

## Packages

| Package | Purpose | Status |
|---|---|---|
| [`@eudi-verify/server`](https://github.com/eudi-verify/eudi-verify/tree/main/packages/server) | REST API handlers, token verification, rate limiting | Preview (MockEngine), Node.js 22+ |
| [`@eudi-verify/embed`](https://github.com/eudi-verify/eudi-verify/tree/main/packages/embed) | Drop-in `<eudi-verify>` web component | Preview |
| [`@eudi-verify/client`](https://github.com/eudi-verify/eudi-verify/tree/main/packages/client) | Typed API client, state machine, QR generation | Preview |
| [`@eudi-verify/react`](https://github.com/eudi-verify/eudi-verify/tree/main/packages/react) | React wrapper with typed props | Preview |

## Status

**Preview release.** Feature-complete for integration development. Not yet audited for production identity verification; production EUDI Wallets expected Dec 2026.

---

See the [current limitations](https://github.com/eudi-verify/eudi-verify#current-limitations) and [supported platforms](https://github.com/eudi-verify/eudi-verify/blob/main/docs/SUPPORTED.md).

This project is for developers, product teams, and integrators who want to prepare for EUDI Wallet verification flows before production wallets are broadly available.

## Get started

**Requirements:** Node.js 22+, [pnpm](https://pnpm.io/).

**1. Clone and build packages** — repository root only (`eudi-verify/`):

```bash
git clone https://github.com/eudi-verify/eudi-verify.git
cd eudi-verify
pnpm install && pnpm build
```

`pnpm build` compiles `packages/*`. Folders under `examples/` only have `start` — no `build` script.

**2. Terminal 1 — shared API server** (new terminal; `cd` to your clone root first):

```bash
cd examples/server && pnpm start
```

**3. Terminal 2 — HTML demo** (another new terminal; clone root):

```bash
cd examples/html-vanilla && pnpm start
```

Open `http://localhost:3001` for the live demo.

Full documentation, architecture, API reference, and integration guide are in the [main repository](https://github.com/eudi-verify/eudi-verify).

---

## Contributing

Contributions are welcome — fixes, examples, tests, documentation, and real-world integration feedback. See the [contributing guide](https://github.com/eudi-verify/eudi-verify/blob/main/CONTRIBUTING.md) and [code of conduct](https://github.com/eudi-verify/eudi-verify/blob/main/CODE_OF_CONDUCT.md).

---

## License

AGPL-3.0. Commercial licenses available. See [licensing details](https://github.com/eudi-verify/eudi-verify/blob/main/LICENSING.md).
