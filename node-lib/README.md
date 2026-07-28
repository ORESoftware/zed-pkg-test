# node-lib (zed-pkg-test/node-lib)

A trivial Node library published to the zed registry. Consumers source it **via
zed** (into their configured `[install].dir`) while npm keeps owning the rest of
`node_modules`. See `.zpkg.toml`. It also carries a normal `package.json` so
Node resolves it once zed drops it into place.
