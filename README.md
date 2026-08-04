# zed-pkg-test

Integration fixtures and independent certification for the Zed package ecosystem.

## Zed CLI cross-repository certification

`zed-cli-ref.txt` pins the exact `zed-pkg/zed-cli` commit under review. The
`Zed CLI submodule interoperability certification` workflow checks out that
immutable commit without persisted credentials and runs:

- strict Rust formatting;
- Git-submodule unit tests;
- real-binary mixed-repository, CLI/environment, rollback, branch-provenance,
  and fresh-clone frozen-replay tests on Ubuntu and macOS; and
- all-target Clippy with warnings denied on Ubuntu.

Updating the pinned SHA through a pull request provides an independent execution
signal outside the `zed-pkg/zed-cli` repository's own workflow queue.
