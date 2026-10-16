# healary-kill-switch

The static copy of the Healary app's certificate-pinning kill-switch config (FITSY-42959,
ADR-0034 in Healary/HealaryCrossPlatform), served by GitHub Pages at
`https://healary.github.io/healary-kill-switch/kill-switch.json`.

The app reads it, together with the copy on the backend's unpinned alias host, when a pinned host
fails. The file is public on purpose: it is signed offline with an Ed25519 key the app knows, and
the app ignores anything that does not verify, has expired, or is older than the last version it
accepted. Only `kill-switch.json` is read.

How to sign and publish a config: `scripts/kill-switch/README.md` in Healary/HealaryCrossPlatform.
