# Abdul Afif Al Kaysan

I'm Abdul Afif Al Kaysan, a builder in Bandung, Indonesia. I build quant
research systems, web3 security tooling, and Android/kernel tooling — and I
publish the negative results, not just the wins.

Every claim below is checkable in the linked repository.

## Selected work

**[arbitrage-research](https://github.com/beduldul/arbitrage-research)** — Measured
arbitrage research across 10+ classes on real public order books, at a $100
retail basis.
→ The verdict is negative: no class is net-positive, because the retail
fee/spread floor — not the absence of signal — defeats every one. The
methodology documents three of the project's own measurement artifacts caught
before they became claims.

**[honest-backtest](https://github.com/beduldul/honest-backtest)** — Statistical
guards that refuse to certify a backtest you have fooled yourself with.
→ 301 tests pass in CI, each guard written from a specific false positive it
caught in the author's own research.

**[rfc5322](https://github.com/beduldul/rfc5322)** — An RFC 5322-conformant email
address parser (full obsolete §4.4 grammar), zero runtime dependencies.
→ 263 tests, 98% coverage, CI green on Python 3.12 and 3.13.

**[chainguard-web3-security](https://github.com/beduldul/chainguard-web3-security)** —
Next.js web3 security dashboard that simulates and risk-scores EVM and Solana
transactions before signing, with a companion set of onchain contracts.
→ 8 Solidity contracts under Foundry; 91 tests passing, CI green.

**[dns-shield](https://github.com/beduldul/dns-shield)** — Diagnoses ISP DNS
poisoning and works around it with DNS-over-HTTPS resolution and
SNI-preserving connections.
→ 289 tests passing; stdlib only, no runtime dependencies.

**[gki-abi-checker](https://github.com/beduldul/gki-abi-checker)** — Android GKI
ABI compatibility checker for kernel `.config` files and source definitions.
→ Validates memory-layout flags (e.g. `CONFIG_SLUB_DEBUG`) whose change would
shift `struct page` and bootloop a GKI device. MIT.

## What I'm looking for

Open to work, contract, and research collaboration in quant research, web3
security, and Android/kernel tooling.

## Tooling

Python · TypeScript / JavaScript · Solidity · Shell · Java · C — with pytest,
Foundry, Node.js, GitHub Actions, and Linux/Android kernel tooling.

## Contact

- Email: alkaysan07@gmail.com
- GitHub: [@beduldul](https://github.com/beduldul)
