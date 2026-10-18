# Security Policy (安全策略)

## Reporting a vulnerability

Please do **not** open a public issue for security problems. Report privately to the repository owner.

We commit to:

- **Never storing secrets in repositories** — credentials live in a local DPAPI vault (`~/.ucvault_local`), never in chat, command line, files, or sync packages.
- Treating leaked credentials as EXPOSED_PENDING_ROTATION until rotated.
- Reviewing reports within 7 days and responding with next steps.

## Secrets discipline (凭证纪律)

- API keys / tokens / passwords: vault only, per the shared credential ledger (`01-密钥状态_跨账号台账.md`).
- Live verification before use; ledger is source of truth for status.
- Never paste a secret into chat, issue, PR, or log output.

## Dependency and supply-chain notes

Where a repository uses third-party actions or packages, pin versions and review changes; provenance attestation is preferred (see attest-build-provenance where configured).

*This policy is self-reported and AS IS; it is not a certification.*
