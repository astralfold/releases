# astralfold releases

Signed release packages of Orbit (the sun) and its modules. The code repositories are private; this repository holds only the release assets.

Each GitHub Release is tagged `<key>-<version>` (the sun: `sun-<version>`) and carries three assets:

- `<key>@<version>.zip` – the release
- `<key>@<version>.json` – its description, with the resolved build configuration
- `<key>@<version>.zip.sig` – a minisign signature (Ed25519) over a statement naming key, version, platform and the sha-256 of zip and json

An Orbit installation fetches releases from here and installs one only when its signature checks against the public keys it was installed with. The format is described in `docs/sun-update-formats.md` §9 of the Orbit framework.
