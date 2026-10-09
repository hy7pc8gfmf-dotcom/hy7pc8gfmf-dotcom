# Constructive formalization portfolio | 构造性形式化作品集

Formal mathematics in Rocq/Coq: constructive analysis with extractable witnesses, certified systems, and the CI infrastructure to keep them honest — built long-term, in the open.

## Headline work | 代表作

**Constructive pi for the Rocq standard library** — the first concrete constant and first analytic theorem for the constructive Cauchy reals layer:

- pi is apart, with explicit witnesses, from every rational (`CReal_appart`), stated **premise-free**
- 24 new files, ~35.1K lines; zero axioms (`coqchk` → `Axioms: <none>`); zero compiler warnings; extraction with `Obj.magic = 0`
- zero-failure CI across Rocq 9.1 / 9.2 / 9.3 / Alpine (master bundle: zero failures, heavies at tail)
- Upstream: [PR #316](https://github.com/rocq-prover/stdlib/pull/316) · [PR #313 (engine)](https://github.com/rocq-prover/stdlib/pull/313) · [Issue #312](https://github.com/rocq-prover/stdlib/issues/312)
- Long-term maintenance committed: compatibility upkeep across future Rocq releases, review responses within days.

## Ongoing libraries | 在营库

| repo | what | 说明 |
|---|---|---|
| [ConstructiveWorld-Main](https://github.com/hy7pc8gfmf-dotcom/ConstructiveWorld-Main) | modular trust-cache constructive library (base line) | 模块化信任缓存构造库·基座线 |
| [ConstructiveWorld-Set](https://github.com/hy7pc8gfmf-dotcom/ConstructiveWorld-Set) | statement-face Set-ification mirror line | 语句面 Set 化镜像线 |
| [PSA-CertifiedSparseGating](https://github.com/hy7pc8gfmf-dotcom/PSA-CertifiedSparseGating) | certified sparse gating for attention — Coq formalization | 注意力认证稀疏门控·Coq 形式化 |
| [Probability](https://github.com/hy7pc8gfmf-dotcom/Probability) | autonomous-driving safety verification over a probability library | 基于概率库的自动驾驶安全验证 |
| [FRF-Zero-Analysis](https://github.com/hy7pc8gfmf-dotcom/FRF-Zero-Analysis) / [2](https://github.com/hy7pc8gfmf-dotcom/FRF-Zero-Analysis-2) | FRF zero-point analysis | FRF 零点分析 |
| [Complex-Analysis](https://github.com/hy7pc8gfmf-dotcom/Complex-Analysis) | complex analysis formalization (early) | 复分析形式化（早期） |

## How I work | 工作方式

Long campaigns with mechanical verification at every step: `coqchk`, `Print Assumptions`, extraction differential + runalive, and zero-failure CI across four Rocq toolchains. Public, review-ready submissions — dependencies mapped, per-module summaries provided, splits prepared.

中文摘要：在 Rocq/Coq 上做构造性形式化——构造实数层首位具体常数 π（逐有理数分离见证·可提取运行）、认证稀疏门控、自动驾驶安全验证等；全流程机械验证（coqchk 零公理·提取零魔数·四工具链 CI 零失败），长期公开维护。
