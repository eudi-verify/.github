# eudi-verify

Open source tools for integrating with the European Digital Identity Wallet.

## What we build

**[eudi-verify](https://github.com/eudi-verify/eudi-verify)** is a framework-agnostic verifier kit for websites and services that want to accept EUDI Wallet credentials.

Think of it as a reCAPTCHA-style integration: a small embeddable widget starts a wallet verification flow and returns a server-verifiable token.

```html
<!-- Age verification in any HTML page -->
<eudi-verify api-url="/api/eudi" request='{"age_over_18": true}'></eudi-verify>
```

**Live demo:** https://demo.eudi-verify.eu/

## Packages

| Package | Purpose |
|---|---|
| [`@eudi-verify/server`](https://github.com/eudi-verify/eudi-verify/tree/main/packages/server) | REST API handlers for Node.js 22+ |
| [`@eudi-verify/embed`](https://github.com/eudi-verify/eudi-verify/tree/main/packages/embed) | Drop-in `<eudi-verify>` web component |
| [`@eudi-verify/client`](https://github.com/eudi-verify/eudi-verify/tree/main/packages/client) | Typed client SDK for custom UIs |
| [`@eudi-verify/react`](https://github.com/eudi-verify/eudi-verify/tree/main/packages/react) | React wrapper with typed props |

## Use cases

- Age verification without collecting ID documents
- Credential-based access control
- Scoped identity attribute verification
- EUDI Wallet integration prototyping

## Status

**Active development / demo mode.** The wallet side is currently simulated because production EUDI Wallets are not yet generally available. This is for integration preparation and prototyping — not production identity verification yet.

See the [current limitations](https://github.com/eudi-verify/eudi-verify#current-limitations) and [supported platforms](https://github.com/eudi-verify/eudi-verify/blob/main/docs/SUPPORTED.md).

## Why this exists

The EUDI Wallet ecosystem is emerging under the eIDAS 2.0 Regulation. Websites and service providers can prepare their integration architecture before production wallets are broadly available.

This project provides a small, auditable verifier kit with clear boundaries: an OpenAPI contract, a Node.js reference implementation, typed client libraries, and drop-in frontend widgets.

## Get started

```bash
git clone https://github.com/eudi-verify/eudi-verify.git
cd eudi-verify
pnpm install && pnpm build
cd examples/server && pnpm start &
cd ../html-vanilla && pnpm start
```

Open `http://localhost:3001` for the demo.

See the [integration guide](https://github.com/eudi-verify/eudi-verify/blob/main/docs/INTEGRATION.md) for production-like setup.

## Contributing

Contributions are welcome. Read the [contributing guide](https://github.com/eudi-verify/eudi-verify/blob/main/CONTRIBUTING.md) and [code of conduct](https://github.com/eudi-verify/eudi-verify/blob/main/CODE_OF_CONDUCT.md).

Ways to help:
- Try the demo and open issues
- Contribute fixes, examples, or tests
- Share feedback from real integration scenarios
- Improve documentation

## Resources

- **Main repository:** [eudi-verify/eudi-verify](https://github.com/eudi-verify/eudi-verify)
- **Documentation:** [Architecture](https://github.com/eudi-verify/eudi-verify/blob/main/README.md#architecture) · [API spec](https://github.com/eudi-verify/eudi-verify/blob/main/openapi/eudi-verifier.yaml) · [Security](https://github.com/eudi-verify/eudi-verify/blob/main/SECURITY.md) · [Roadmap](https://github.com/eudi-verify/eudi-verify/blob/main/docs/PLAN.md)
- **Demo:** https://demo.eudi-verify.eu/
- **Discussions:** [GitHub Discussions](https://github.com/eudi-verify/eudi-verify/discussions)

## License

AGPL-3.0 — free to use and host, even commercially. If you modify the verifier, you must share your changes. Commercial licenses available if you need to keep modifications proprietary — see [licensing details](https://github.com/eudi-verify/eudi-verify#license).

---

**Official EU resources:**
- [European Digital Identity Wallet — European Commission](https://ec.europa.eu/digital-building-blocks/sites/spaces/EUDIGITALIDENTITYWALLET/pages/694487738/EU+Digital+Identity+Wallet+Home)
- [EUDI Wallet Architecture and Reference Framework](https://eu-digital-identity-wallet.github.io/eudi-doc-architecture-and-reference-framework/)
