# How smooth can the 547/727 prime race be?

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24413211.svg)](https://doi.org/10.5281/zenodo.24413211)

This result is now maintained in [theta-host-split-inert-race](https://github.com/leecrossley/theta-host-split-inert-race/tree/main/results/theta-race-width-regularity). This repository is archived and keeps its releases and DOI.

Every nonzero finite combination of aligned window widths has the same mean-square regularity threshold, even if some widths have negative weights. Its limiting prime-race profile has spectral Sobolev order $`s`$ exactly for $`s\lt 3/2`$. At small log displacement $`h`$, the root-mean-square second difference is of order **$`h^{3/2}\sqrt{\log(1/h)}`$**. The result includes every positive average of widths with compact support. [Theorem and proof](PROOF.md)

A signed continuous average can produce a profile with derivatives of every order. Given any smooth compactly supported function of positive log distance, the proof gives an explicit weighting of widths that realizes its symmetric prime-ideal sum **at every finite height**. A nonzero example has a Fourier coefficient above one tenth. [Kernel construction](PROOF.md#constructing-a-smooth-race-at-every-height)

At width two the largest limiting second difference is of order $`h\log(1/h)`$. The new mean-square bound implies that, for any fixed fraction of that maximum, the upper log density of heights reaching it in absolute value is $`O(h/\log(1/h))`$. All estimates allow repeated or shared zeros among the eight underlying factors. [Peak curvature](https://github.com/leecrossley/theta-race-width-cusp/blob/52eee965886958193d2ff38595f92389b90f4b93/PROOF.md#the-cusp-at-every-width) · [Prior work](PRIOR-WORK.md)

For a signed combination of widths two and four whose constant spectral numerator cancels, the mean numerator square over high zero ordinates tends to $`172/25`$. The release also certifies six finite lower bounds using 782 sign-changing zero brackets and checks the finite-height construction directly at geometric centres 31, 100 and 250. [Finite checks](evidence/check.txt)

## Replay

In a Python 3.10+ virtual environment run

```sh
python -m pip install -r requirements.txt
python shell_energy.py
python synthesis.py
python independent.py
python check_source.py
```

On x86-64 Linux with Git, curl, tar and zstd, `bash verify-release.sh` also verifies the manifest, upstream records and five Lean deductions. With Lean 4.33.1 on PATH and Mathlib at commit `0df444a360eaa60ab8c11dca51a86af692955474`, run `bash verify-release.sh /path/to/mathlib4`. An optional second argument supplies the five upstream files. The asymptotic analysis and synthesis have written proofs. [Local Lean deductions](WidthRegularity.lean) · [File hashes](SHA256SUMS)
