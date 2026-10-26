# Constructive formalization portfolio | 构造性形式化作品集

Independent Rocq/Coq formalization work - everything over `Set` carriers, no axioms, extractable witnesses.

## Repositories

- **[rocq-pi-leibniz](https://github.com/hy7pc8gfmf-dotcom/rocq-pi-leibniz)** - Rocq 9.1 formalization of the irrationality of pi via the Leibniz window method. 39 modules, all statements over `Set` carriers, `coqchk` ALL_PASS with `Axioms: none`, extractable with zero `Obj.magic`. DOI: [10.5281/zenodo.23656983](https://doi.org/10.5281/zenodo.23656983) (v1.0.4)
- **[ConstructiveWorld-Set](https://github.com/hy7pc8gfmf-dotcom/ConstructiveWorld-Set)** - statement-face Set-carrier constructive mathematics library with explicit `sigT` witnesses.
- **[ConstructiveWorld-Main](https://github.com/hy7pc8gfmf-dotcom/ConstructiveWorld-Main)** - hosting library and main CI line for the constructive mathematics corpus.

## Verification

Every package ships with machine-checked claims: full-tree `coqchk -o` returning `Axioms: <none>`, witness values asserted in CI, and `Obj.magic`-free extraction surfaces.
