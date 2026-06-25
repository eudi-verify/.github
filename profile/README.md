# eudi-verify

Open source tools for integrating with the European Digital Identity Wallet.

Think of it as a reCAPTCHA-style integration: a small embeddable widget starts a wallet verification flow and returns a server-verifiable token — age verification, credential checks, scoped identity attributes, without building the full protocol stack yourself.

```html
<eudi-verify api-url="/api/eudi" request='{"age_over_18": true}'></eudi-verify>
```

**Live demo:** https://demo.eudi-verify.eu/

---

## Packages

| Package                                                                                       | Purpose                               |
| --------------------------------------------------------------------------------------------- | ------------------------------------- |
| [`@eudi-verify/server`](https://github.com/eudi-verify/eudi-verify/tree/main/packages/server) | REST API handlers for Node.js 22+     |
| [`@eudi-verify/embed`](https://github.com/eudi-verify/eudi-verify/tree/main/packages/embed)   | Drop-in `<eudi-verify>` web component |
| [`@eudi-verify/client`](https://github.com/eudi-verify/eudi-verify/tree/main/packages/client) | Typed client SDK for custom UIs       |
| [`@eudi-verify/react`](https://github.com/eudi-verify/eudi-verify/tree/main/packages/react)   | React wrapper with typed props        |

---

## Status

**Preview release.** Feature-complete for integration development. Not yet audited for production identity verification; production EUDI Wallets expected Dec 2026.

---

## Get started

```bash
git clone https://github.com/eudi-verify/eudi-verify.git
cd eudi-verify
pnpm install && pnpm build

# Terminal 1 — shared API server
cd examples/server && pnpm start

# Terminal 2 — HTML demo
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
