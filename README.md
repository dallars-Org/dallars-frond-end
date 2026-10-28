# Vellar Frontend (vellar-dapp)

<img width="5410" height="2088" alt="Full Logo White" src="https://github.com/user-attachments/assets/2eb47ce8-095d-4ce2-b64f-af530b7ce0f9" />

**Vellar** is a web-first Stellar smart wallet with a companion browser extension.
Passkey onboarding (no seed phrases), programmable on-chain account policies,
contract verification & trust signals, and account cleanup/merge tooling.

The SDK that powers Vellar is published separately as
[`vellar-sdk`](https://github.com/Vellar-Wallet/vellar-sdk), with full docs at
**[docs.vellar.xyz](https://docs.vellar.xyz)**.

> **Note**: The codebase is split into two repositories:
> - **Frontend** (`vellar-dapp` / `vellar-frontend`): Web application, companion browser extension, and frontend client SDKs.
> - **Backend** (`vellar-backend`): Backend microservices, Soroban smart contracts, and Docker/infra.

## Layout

- `apps/`:
  - `web`: Next.js web application (onboarding, dashboard, policy builder, verification console, cleanup wizard)
  - `extension`: Chrome/Firefox companion browser extension (WXT + React)
  - `docs`: Product & protocol documentation
- `packages/`:
  - `passkey`: Passkey helpers & error mapping
  - `provider-sdk`: dApp <-> extension protocol and client library
  - `types`: Domain types
  - `ui`: Shared UI component library
  - `verification-sdk`: Contract verification SDK

## Getting started

```sh
pnpm install
pnpm build
```

## Running locally

```sh
# Run web app only
pnpm --filter=@vellar/web dev

# Run web app + browser extension
pnpm dev
```

## License

Apache-2.0 — see [LICENSE](LICENSE).
