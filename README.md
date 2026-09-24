# Abdul Afif Al Kaysan · `beduldul`

Python systems — ML infrastructure, quantitative analysis, and auditing of measurement code.

I build systems that collect data and make predictions, then spend most of my time trying to
falsify the numbers they produce. Most of this work is private; the audits are what I show.

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/) [![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)](https://pandas.pydata.org/) [![XGBoost](https://img.shields.io/badge/XGBoost-006ACC?style=flat-square&logo=xgboost&logoColor=white)](https://xgboost.readthedocs.io/) [![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)](https://scikit-learn.org/) [![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/) [![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white)](https://www.sqlalchemy.org/) [![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)](https://sqlite.org/) [![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://www.postgresql.org/) [![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)](https://pytest.org/) [![Ruff](https://img.shields.io/badge/Ruff-D7FF64?style=flat-square&logo=ruff&logoColor=black)](https://docs.astral.sh/ruff/) [![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)](https://nextjs.org/) [![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/) [![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)](https://playwright.dev/) [![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/) [![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)](https://kernel.org/)

## Selected work

**NEXUS — ML-first crypto trading system** *(private)*
~17k lines of Python 3.12 across `engine/`, `agents/`, `strategies/`, `collector/`, `api/`.
XGBoost models are trained on *simulated outcomes under the production exit engine*, not on
"will price go up". Probabilities are Platt-calibrated (`CalibratedClassifierCV`) and measured
by AUC, log-loss and Brier score, against a separate walk-forward engine that slides
alternating train/test windows with no future leakage. ~1,900 model artifacts came out of the
search. A hardening pass found and fixed 12 bugs where gates could be bypassed, local and
exchange position state could diverge, or a failed stop-loss left a live position unhedged.
123 tests passing. `fastapi`, `sqlalchemy`, `alembic`, `pandas`, `ccxt`, `structlog`.

**Signal audit — why a model wasn't learning** *(private)*
Audited the 12-feature featurizer feeding an FTRL model against 1.18M recorded tick rows. One
feature (`z8`) consumed **99.63%** of the gradient: a self-referential normaliser whose z-score
is computed against a sample excluding the point being scored, inflating it to ±7.2e5. Also
three dead slots (normalisers saturating to 1.0), a duplicated feature, one exactly collinear
feature (`mom5_20 == ret20 − ret5`, verified over 146,280 rows), and a feature/label horizon
mismatch — features in event ticks, labels in 2-second wall-clock ticks. Repairing `z8` moved
AUC 0.5068 → 0.5149: real, and still indistinguishable from noise. Two findings, not conflated.

**Rejecting a headline edge I couldn't reproduce** *(private)*
A prior analysis reported a **+0.76c/share** favourite-longshot edge (n=2,122, t=+2.15). I
found the exact line manufacturing it: a hardcoded `min(0.98, ask)` entry-price cap that
inflated every zone by +1.23–1.33c. Recomputed honestly, the published figure sat between the
mid fantasy and the real ask without being either.

**Execution cost and adverse selection** *(private)*
Streamed 18 days of quote snapshots (1.5M ticks/day) to price out maker entries. The naive
"market came to you" fill proxy was measuring **book repricing, not executions** — the whole
book dropping together; genuine fills at a resting bid are ~0.13% of ticks. Real fills show
adverse selection of −2.31c at 30s (t = −3.46) against a 0.5c median spread saving.

**Reconcile audit — three ledgers, no agreement** *(private)*
Reconstructed FIFO PnL from 314 raw fills. The fills table, the equity curve and the bot's
internal ledger are three mutually inconsistent records (realized −4.38 / −3.71 / −12.14).
Root cause: a 12-hour restore horizon silently dropped older BUY fills, leaving 20 tokens /
353.7 shares / $174.51 orphaned with no exit path — a warning the log had fired 591 times.
Fixed, with a regression test. A second candidate bug was investigated and deliberately
**not** fixed: simulating the exact fill arithmetic showed it discards $0.00.

**Attendance automation — Playwright at scale** *(private)*
Playwright contexts driving an SSO/MFA portal for a cohort of ~97 students. Credentials are
Fernet-sealed with the master key only in the environment, and a preflight check exits
`EX_CONFIG` *before* any network call so a bad key cannot burn Microsoft login attempts across
every account. systemd on a VPS provisioned by script (key-only SSH, fail2ban, UFW). The README
corrects its own earlier memory number: ~82 MB was an empty context, a real page is ~136 MB.

**ThermoApp — thermodynamic phase-equilibrium app for macOS** *(public)*
SwiftUI front end over `pycalphad`, for binary phase diagrams and reaction equilibria.

**Android systems tooling** *(public)*
A set of kernel- and userspace-level utilities: GKI ABI compatibility verification, SELinux
runtime policy injection, a Magisk/KernelSU module packaging and validation tool, and a
performance daemon. Mostly Python and POSIX shell against real kernel interfaces.

## How I work

Build the system, then try to falsify the numbers it produces. I would rather report "this
edge is an artifact of a hardcoded price cap" than keep a flattering result, and I keep
"the bug explains the failure to learn" separate from "the bug was hiding a signal", because
those are different claims. Off-by-one bugs in a featurizer and a wrong constant in a README
get the same treatment.

Work is reproducible: audit findings live in committed markdown next to the exact command that
regenerates them, and scope limits (partial date ranges, sample sizes) are stated rather than
omitted. Typical stack: typed Python 3.12 with `ruff` and `pytest`, async FastAPI + SQLAlchemy
over SQLite/Postgres with Alembic, XGBoost/scikit-learn for modelling.

## Contact

[alkaysan07@gmail.com](mailto:alkaysan07@gmail.com)
