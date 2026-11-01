# Constructive formalization portfolio | 构造性形式化作品集

Formal mathematics in Rocq/Coq: constructive analysis with extractable witnesses, certified systems, and the CI infrastructure to keep them honest — built long-term, in the open.

## Lines | 三条线

| repo | CI | license · version | state |
|---|---|---|---|
| [rocq-pi-leibniz](https://github.com/hy7pc8gfmf-dotcom/rocq-pi-leibniz) | [![CI](https://github.com/hy7pc8gfmf-dotcom/rocq-pi-leibniz/actions/workflows/ci.yml/badge.svg)](https://github.com/hy7pc8gfmf-dotcom/rocq-pi-leibniz/actions/workflows/ci.yml) | LGPL-2.1 · v1.0.4 (main beyond) | 41 modules · zero axioms · extractable witnesses · **√2 uniform strong irrationality landed (Bishop-form)** · [DOI](https://zenodo.org/doi/10.5281/zenodo.23527294) |
| [ConstructiveWorld-Main](https://github.com/hy7pc8gfmf-dotcom/ConstructiveWorld-Main) | — | Apache-2.0 | base line · 857 registered modules · content-addressed attestation live (archive-hit → skip-list before coqchk) · run #318 green · KB70 leafification landing in flight |
| [ConstructiveWorld-Set](https://github.com/hy7pc8gfmf-dotcom/ConstructiveWorld-Set) | — | Apache-2.0 | statement-face Set-carrier mirror · ~160 modules across waves M29–M38 · gate7 born-clean law operational (two interceptions, two cures) · W3 report-only live · queue-mode CI |

[PSA-CertifiedSparseGating](https://github.com/hy7pc8gfmf-dotcom/PSA-CertifiedSparseGating) — certified sparse gating for attention: Coq formalization (165-entry audit, zero classical axioms) + empirical scripts + papers; CI green. [![Coq CI](https://github.com/hy7pc8gfmf-dotcom/PSA-CertifiedSparseGating/actions/workflows/coq.yml/badge.svg)](https://github.com/hy7pc8gfmf-dotcom/PSA-CertifiedSparseGating/actions/workflows/coq.yml)

Badge rule: a CI badge is worn only while the latest completed run on the line is green — at this edit the π line's run is in flight (the badge renders its live state), and Main/Set are mid-run, so their badges return when their current runs land green. This is rule, not omission.

## Flagship | 旗舰件：constructive pi

**[rocq-pi-leibniz](https://github.com/hy7pc8gfmf-dotcom/rocq-pi-leibniz) v1.0.4** — a constructive pi for the constructive Cauchy reals of the Rocq standard library: premise-free separation of pi from every rational, with explicit, extractable, runnable witnesses. Upstream: [PR #316](https://github.com/rocq-prover/stdlib/pull/316), stacked on [PR #313 (engine)](https://github.com/rocq-prover/stdlib/pull/313) · [issue #312](https://github.com/rocq-prover/stdlib/issues/312). [DOI 10.5281/zenodo.23527294](https://zenodo.org/doi/10.5281/zenodo.23527294) · opam package `rocq-pi-leibniz` · LGPL-2.1.

41 modules on the main line (40 content modules plus the root re-export). Claims, each checkable on your machine:

1. **Zero axioms.** `coqchk -o` over the whole dependency closure: *Modules were successfully checked*, assumption summary all-none; `Print Assumptions` on both main theorems reports *Closed under the global context*.
2. **Witness values asserted in CI.** Documented sample points are computed on every run by `vm_compute`: the escape witness triple for `q = 22 # 7` evaluates to `(22 # 7, 5 # 8, 3) : Q * Q * nat` — explicit margin `5 # 8`, threshold index `3`. Green or the badge comes off.
3. **Extraction carries no escape hatch.** Statement faces are Set-carried (`QltT`/`QeqT` carrier block, 238 Set-carried twin faces in the kernel-slack file); the extracted OCaml has `Obj.magic = 0` and zero statement-name loss. Legacy `Prop` supply lemmas are migrating to Set carriers wave by wave; the main theorems stay on the stdlib face until the full Set replacement lands.
4. **New on main: the uniform-type strong irrationality of √2 as a formalized entity** — `Sqrt2UniformStrongIrrational` (Bishop-form explicit margin 1/(3b²), `sigT` Set-carried, four witness-value assertions, 1,523 lines, extraction dual-face `Obj.magic` = 0); cloud certification in flight.

From a Rocq 9.1+ opam switch:

```sh
git clone https://github.com/hy7pc8gfmf-dotcom/rocq-pi-leibniz && cd rocq-pi-leibniz
opam pin add rocq-pi-leibniz . -y   # then: Check pi_leibniz_appart_all_Q.
```

## Also on this account | 其他公开件

- [Probability](https://github.com/hy7pc8gfmf-dotcom/Probability) — autonomous-driving safety verification over a probability library | 基于概率库的自动驾驶安全验证
- [FRF-Zero-Analysis](https://github.com/hy7pc8gfmf-dotcom/FRF-Zero-Analysis) / [2](https://github.com/hy7pc8gfmf-dotcom/FRF-Zero-Analysis-2) — FRF zero-point analysis | FRF 零点分析
- [Complex-Analysis](https://github.com/hy7pc8gfmf-dotcom/Complex-Analysis) — complex analysis formalization (early) | 复分析形式化（早期）

## How I work | 工作方式

Long campaigns with mechanical verification at every step: `coqchk`, `Print Assumptions`, extraction differential + runalive, and zero-failure CI across four Rocq toolchains. Public, review-ready submissions — dependencies mapped, per-module summaries provided, splits prepared. Numbers on this page are re-checked against the repos before every edit; nothing green is claimed from memory.

中文摘要：在 Rocq/Coq 上做构造性形式化——旗舰件：构造实数层首位具体常数 π（逐有理数分离·见证可提取可运行·coqchk 零公理·提取零魔数·CI 断言见证值；v1.0.4 · 41 模块 · [DOI](https://zenodo.org/doi/10.5281/zenodo.23527294) · 上游 stdlib PR #316/#313）·新增上岸：**√2 一致型强无理形式化实体**（Bishop 形显式余项 1/(3b²)·sigT Set 承载·提取双面零魔数·云认证在飞）；认证稀疏门控（165 条审计·零经典公理）；双线在营：ConstructiveWorld 基座线（857 在册模块·内容寻址认证在役·run #318 绿·KB70 叶化落地在飞）与 Set 镜像线（~160 件·M29–M38 波·gate7 born-clean 律运行·W3 report-only 在役·队列模式 CI）。全流程机械验证（coqchk 零公理·提取零魔数·四工具链 CI 零失败），徽章只挂当下绿 run，长期公开维护。
