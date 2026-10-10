# Abdul Afif Al Kaysan

I'm Abdul Afif Al Kaysan, a builder in Bandung, Indonesia. I build quant
research systems, web3 security tooling, and Android/kernel tooling — and I
publish the negative results, not just the wins.

Every claim below is checkable in the linked repository.

## Languages

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-DEA584?style=flat-square&logo=rust&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Solidity](https://img.shields.io/badge/Solidity-363636?style=flat-square&logo=solidity&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Swift](https://img.shields.io/badge/Swift-F05138?style=flat-square&logo=swift&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnu-bash&logoColor=white)

Every badge is backed by code: Python — rfc5322, pdfua, dns-shield,
calphad-io, honest-backtest, arbitrage-research, attendance-bot, ThermoApp,
aloy-alloy-design; Rust — solguard and the vaultguard Anchor programs (Solana
programs are Rust, not Solidity); TypeScript — chainguard-web3-security
dashboard; Solidity — the chainguard-web3-security EVM contracts only;
JavaScript — chainguard plus vite-hmr-doctor and pancasila; Swift — the
ThermoApp macOS app; Java — hyperspeed-engine; Bash — the Android GKI tuning
and build tooling scripts.

## Published on PyPI

Four of these are packaged and installable, published under the PyPI account
[`bedul`](https://pypi.org/user/bedul/):

- **[rfc5322](https://pypi.org/project/rfc5322/)** `1.0.1` — RFC 5322 conformant
  email address parser with the full obsolete §4.4 grammar; dependency-free
  (Python 3.12+).
  `pip install rfc5322`
- **[pdfua](https://pypi.org/project/pdfua/)** `0.1.2` — Checks the
  machine-checkable subset of PDF/UA-1 and WCAG 2.1 in PDFs, built on pikepdf
  with no JVM (Python 3.10+).
  `pip install pdfua`
- **[dns-shield](https://pypi.org/project/dns-shield/)** `0.1.2` — Detects ISP
  DNS poisoning and works around it with DNS-over-HTTPS and SNI-preserving
  connections (Python 3.10+).
  `pip install dns-shield`
- **[calphad-io](https://pypi.org/project/calphad-io/)** `0.1.2` — Reads, writes
  and validates CALPHAD thermodynamic databases (Thermo-Calc `.TDB`,
  ChemSage/FactSage `.DAT`) (Python 3.10+).
  `pip install calphad-io`

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
→ Each guard was written from a specific false positive it caught in the
author's own research; 301 tests pass locally, CI green.

**[rfc5322](https://github.com/beduldul/rfc5322)** — The parser behind the PyPI
package above: an RFC 5322-conformant email address parser (full obsolete §4.4
grammar), zero runtime dependencies.
→ 288 tests, 99% coverage, CI green.

**[chainguard-web3-security](https://github.com/beduldul/chainguard-web3-security)** —
Next.js web3 security dashboard that simulates and risk-scores EVM and Solana
transactions before signing, with a companion set of onchain contracts.
→ A set of Solidity contracts under Foundry, with CI green.

**[dns-shield](https://github.com/beduldul/dns-shield)** — The diagnostics and
DNS-over-HTTPS workaround behind the PyPI package above, for ISP DNS poisoning.
→ 299 tests passing (4 opt-in live tests deselected); stdlib only, no runtime
dependencies.

**[gki-abi-checker](https://github.com/beduldul/gki-abi-checker)** — Android GKI
ABI compatibility checker for kernel `.config` files and source definitions.
→ Validates memory-layout flags (e.g. `CONFIG_SLUB_DEBUG`) whose change would
shift `struct page` and bootloop a GKI device. MIT.

## What I'm looking for

Open to work, contract, and research collaboration in quant research, web3
security, and Android/kernel tooling.

## Tooling

pytest · Foundry · Anchor · Node.js · GitHub Actions · SQLite · Docker —
across the Python research stack, the Rust/Solidity security tooling, and
Linux/Android kernel work (shell scripts, kernel `.config` tooling, Magisk
module builds).

## Contact

- Email: alkaysan07@gmail.com
- GitHub: [@beduldul](https://github.com/beduldul)
