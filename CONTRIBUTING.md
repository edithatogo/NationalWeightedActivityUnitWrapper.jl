# Contributing to NationalWeightedActivityUnitWrapper.jl

Contributions improve NationalWeightedActivityUnitWrapper, the thin Julia wrapper around the MCHS/NWAU command boundary. Calculation formulas remain outside this package.

## Before you start

Read the [README](README.md), [Julia project manifest](Project.toml), and [existing tests](test/runtests.jl). Explain how a change affects CSV validation, CLI argument construction, execution, or returned output paths.

Search existing issues and pull requests to avoid duplicating work. Describe substantial proposals before implementation, and use repository issue or pull request templates when available. Small corrections can go directly into a focused pull request.

For bug reports, include the affected version or commit, environment, minimal reproduction, expected and actual behavior, and sanitized diagnostics. For feature requests, explain the use case and intended outcome.

## Development and validation

Use the Julia compatibility range declared in `Project.toml`, which currently specifies Julia 1.10 compatibility. The manifest declares the standard `Test` dependency and test target; the checked-in suite covers command assembly and the missing-input guard.

Run the declared package tests in that project environment and record the exact invocation, Julia version, and result. Add synthetic regression cases for changed argument ordering, paths, year handling, or validation failures. Distinguish wrapper tests from end-to-end execution of the external calculator, which requires a separately available CLI and parameter files.

Preserve the package's orchestration-only boundary. Do not introduce independent reimbursement formula logic or claim that passing wrapper tests validates an economic calculation. Document any change to the external command contract and downstream compatibility.

Update affected documentation and examples alongside behavior changes. Add a focused regression case for a bug fix where executable tests are appropriate. Record checks that were not run and the reason.

## Submitting a pull request

Create a focused branch from the current `main` branch and open a pull request back to it. Keep unrelated formatting, refactoring, and dependency changes separate.

Include:

- The problem, proposed change, and resulting behavior.
- Related issues or existing track references.
- Exact validation commands or inspection steps, results, and limitations.
- Compatibility implications and any data or dependency provenance.

Inspect the complete diff before submission. Required automated checks must pass before merge. Follow the existing repository and account policies; this guide does not introduce a second-person approval requirement or relax existing checks.

## Security and sensitive information

Follow the [account security policy](https://github.com/edithatogo/.github/blob/main/SECURITY.md). Report vulnerabilities privately through GitHub's **Report a vulnerability** option if available. Otherwise request a private reporting contact without disclosing the vulnerability publicly. Keep credentials, personal data, and unredacted logs out of commits, issues, and examples.

## Licensing and conduct

Respect the [existing license](LICENSE) and preserve third-party notices. Submit only material you are entitled to contribute, and document unclear permissions before adding third-party content. Follow the [account code of conduct](https://github.com/edithatogo/.github/blob/main/CODE_OF_CONDUCT.md). This guide adds no CLA, mandatory sign-off, or relicensing condition.

## Reference guidance

- [GitHub contributor guidelines](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/setting-guidelines-for-repository-contributors)
- [OpenSSF Best Practices criteria](https://www.bestpractices.dev/en/criteria)
