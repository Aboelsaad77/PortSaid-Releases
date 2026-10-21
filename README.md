# PortSaid Releases — distribution only

This repository publishes **customer-facing release assets** and the release
metadata the PortSaid Store registry discovers. It contains no source code.

* Assets are attached to GitHub Releases with predictable tags (`v<version>`).
* Every asset carries a sha256 digest. The store refuses to serve a release
  whose digest is missing when the app requires one.
* Signed apps ship a `latest.json` manifest with an Ed25519 detached signature,
  verified against the public key configured for that app.
* Releases are produced only by the central workflow in
  `Aboelsaad77/PortSaid-Release-Workflows`, pinned by commit SHA.
