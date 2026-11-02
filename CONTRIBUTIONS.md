# Open Source Contributions

A collection of my contributions to open-source projects, including testing, API consistency, documentation, and issue reports.

## Pull Requests

### PyTorch

- **[#200575 — TestEqualizeFx: Hardware Classification](https://github.com/pytorch/pytorch/pull/200575)**

  Mark quantization equalization tests as `HardwareClassification.GENERIC`, preserving existing test logic and backend guards.

- **[#202711 — TestDiGraph: Hardware Classification](https://github.com/pytorch/pytorch/pull/202711)**

  Mark device-independent graph tests as `GENERIC` and remove their lint exemption to enable classification checks.

### Ascend / Torch-NPU

**Symbolic Shapes API Tests**

Add four focused tests for constraint construction, rendering, symbolic context, and equality; document why `statically_known_true` needs no NPU-specific adaptation.

| Branch | PR |
| --- | --- |
| `master` | **[#37081](https://gitcode.com/Ascend/pytorch/pull/37081)** |
| `v2.7.1` | [#37151](https://gitcode.com/Ascend/pytorch/pull/37151) |
| `v2.9.0` | [#37167](https://gitcode.com/Ascend/pytorch/pull/37167) |
| `v2.10.0` | [#37168](https://gitcode.com/Ascend/pytorch/pull/37168) |
| `v2.11.0` | [#37170](https://gitcode.com/Ascend/pytorch/pull/37170) |
| `v2.12.0` | [#37171](https://gitcode.com/Ascend/pytorch/pull/37171) |

**DimConstraints API Tests**

Add four tests for congruence rewriting, constraint solving, forced specialization, and diagnostic suggestions; reuse existing `DimDynamic` coverage.

| Branch | PR |
| --- | --- |
| `master` | [#38822](https://gitcode.com/Ascend/pytorch/pull/38822) |
| `v2.7.1` | [#38823](https://gitcode.com/Ascend/pytorch/pull/38823) |
| `v2.9.0` | [#38824](https://gitcode.com/Ascend/pytorch/pull/38824) |
| `v2.10.0` | [#38825](https://gitcode.com/Ascend/pytorch/pull/38825) |
| `v2.11.0` | [#38826](https://gitcode.com/Ascend/pytorch/pull/38826) |
| `v2.12.0` | [#38827](https://gitcode.com/Ascend/pytorch/pull/38827) |

**Documentation**

- [#37174 — Symbolic Shapes API Support](https://gitcode.com/Ascend/pytorch/pull/37174) · `v2.7.1`

  Add five symbolic-shape APIs to the support lists for PyTorch 2.7.1–2.12.0.

- [#38848 — DimConstraints API Support](https://gitcode.com/Ascend/pytorch/pull/38848) · `v2.7.1`

  Document four `DimConstraints` methods and `DimDynamic` across five versioned support lists, with upstream documentation links.

- [#44658 — PowerSGDState.__getstate__ Support](https://gitcode.com/Ascend/pytorch/pull/44658) · `master`

  Add the missing method support entry to four documentation versions and correct the class's inapplicable dtype restrictions.

### Other Projects

- [#2830 — Update commit.rst for AtomGit](https://atomgit.com/openeuler/yocto-meta-openeuler/pull/2830)

  My Good First Issue contribution.

## Issues — Ascend / Torch-NPU

- [#2184 — statically_known_true](https://gitcode.com/Ascend/pytorch/issues/2184)

  Analyze upstream coverage and device dependencies, explaining why no NPU patch or duplicate test is needed.

- [#2431 — DimConstraints.solve / DimDynamic](https://gitcode.com/Ascend/pytorch/issues/2431)

  Document device-independent behavior and distinguish the need for focused `solve` tests from existing `DimDynamic` coverage.

- [#4044 — _pop_saved_tensors_default_hooks](https://gitcode.com/Ascend/pytorch/issues/4044)

  Analyze saved-tensor hook restoration and cleanup; validate temporary NPU adaptations of upstream tests.

- [#4045 — PowerSGDState.__getstate__](https://gitcode.com/Ascend/pytorch/issues/4045)

  Verify state extraction, exclusion of `process_group`, and CPU/NPU tensor preservation; identify the documentation gap.

- [#4046 — torch._assert](https://gitcode.com/Ascend/pytorch/issues/4046)

  Validate bool, NPU tensor, and TorchScript assertion behavior; document device adaptation needs in upstream tests.

- [#4047 — Tensor.ccol_indices](https://gitcode.com/Ascend/pytorch/issues/4047)

  Verify CSC/BSC column indices and device preservation; analyze dependencies that prevent direct reuse of broader sparse tests.

- [#4048 — torch._C._nn._parse_to](https://gitcode.com/Ascend/pytorch/issues/4048)

  Verify argument overloads, device/dtype metadata, dispatch, and invalid inputs for this non-computational parser.

- [#5497 — verify_ninja_availability](https://gitcode.com/Ascend/pytorch/issues/5497)

  Verify tool availability checks, missing-tool errors, subprocess failures, and argument rejection.

- [#5499 — BackwardCFunction.save_for_forward](https://gitcode.com/Ascend/pytorch/issues/5499)

  Validate tensor saving, JVP, and gradients; distinguish upstream CPU/double baselines from supplemental NPU float32 checks.
