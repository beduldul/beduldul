# Abdul Afif Al Kaysan

I'm Abdul Afif Al Kaysan, a builder in Bandung, Indonesia. I build quant
research systems, web3 security tooling, metallurgy/CALPHAD tooling, and
Android/kernel tooling — and I publish the negative results, not just the wins.

## Education

**Institut Teknologi Bandung (ITB)** — undergraduate (S1) in Metallurgical
Engineering (Teknik Metalurgi), Fakultas Teknologi Pertambangan dan Perminyakan
(FTTM). Current work includes CALPHAD database tooling and ML-assisted alloy
design.

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

## Published on PyPI

Four of these are packaged and installable, published under the PyPI account
[`bedul`](https://pypi.org/user/bedul/):

- **[rfc5322](https://pypi.org/project/rfc5322/)** `1.0.1` — RFC 5322 conformant
  email address parser with the full obsolete §4.4 grammar; dependency-free
  (Python 3.12+).
  `pip install rfc5322`
- **[pdfua](https://pypi.org/project/pdfua/)** `0.1.3` — Checks the
  machine-checkable subset of PDF/UA-1 and WCAG 2.1 in PDFs, built on pikepdf
  with no JVM (Python 3.10+).
  `pip install pdfua`
- **[dns-shield](https://pypi.org/project/dns-shield/)** `0.1.3` — Detects ISP
  DNS poisoning and works around it with DNS-over-HTTPS and SNI-preserving
  connections (Python 3.10+).
  `pip install dns-shield`
- **[calphad-io](https://pypi.org/project/calphad-io/)** `0.1.3` — Reads, writes
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

**[solguard](https://github.com/beduldul/solguard)** — Rust static analyser
for Solana/Anchor programs, flags common Anchor security pitfalls before
deployment. CI green.

**[vaultguard](https://github.com/beduldul/vaultguard)** — Anchor Solana
program with 13 tests passing on localnet, CI green.

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

## Machine learning & data

![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat-square&logo=scipy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-AA0000?style=flat-square&logo=xgboost&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![BoTorch](https://img.shields.io/badge/BoTorch-EE4C2C?style=flat-square&logo=botorch&logoColor=white)
![pycalphad](https://img.shields.io/badge/pycalphad-2B5B84?style=flat-square)
![pymoo](https://img.shields.io/badge/pymoo-F9A825?style=flat-square)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat-square&logo=matplotlib&logoColor=white)
![joblib](https://img.shields.io/badge/joblib-1E4252?style=flat-square)

## Web & frontend

![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![framer-motion](https://img.shields.io/badge/framer--motion-0055FF?style=flat-square&logo=framer&logoColor=white)
![lucide-react](https://img.shields.io/badge/lucide--react-F56565?style=flat-square&logo=lucide&logoColor=white)
![Recharts](https://img.shields.io/badge/Recharts-22C55E?style=flat-square&logo=recharts&logoColor=white)

## Python ecosystem

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat-square&logo=pydantic&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![pikepdf](https://img.shields.io/badge/pikepdf-8F1D1D?style=flat-square)
![ccxt](https://img.shields.io/badge/ccxt-1E1E1E?style=flat-square&logo=bitcoin&logoColor=white)

## Web3

![Foundry](https://img.shields.io/badge/Foundry-1E1E1E?style=flat-square&logo=ethereum&logoColor=white)
![Anchor](https://img.shields.io/badge/Anchor-9945FF?style=flat-square&logo=solana&logoColor=white)
![Solana](https://img.shields.io/badge/Solana-9945FF?style=flat-square&logo=solana&logoColor=white)

## Tooling & infra

![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)
![ruff](https://img.shields.io/badge/ruff-261230?style=flat-square&logo=ruff&logoColor=white)
![mypy](https://img.shields.io/badge/mypy-2A6DB2?style=flat-square&logo=mypy&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![nginx](https://img.shields.io/badge/nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![uv](https://img.shields.io/badge/uv-DE5FE9?style=flat-square&logo=uv&logoColor=white)

## Data & storage

![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white)
![Alembic](https://img.shields.io/badge/Alembic-2F2F2F?style=flat-square&logo=alembic&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)

## Contact

- Email: alkaysan07@gmail.com
- GitHub: [@beduldul](https://github.com/beduldul)
