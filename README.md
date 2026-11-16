<!-- The README of github.com/mlreps/homebrew-tap. ⚠ THIS FILE IS THE ORIGINAL (see docs/release/cli-README.md
     for why it lives here rather than in GitHub's editor). Publish it with:
     gh api -X PUT repos/mlreps/homebrew-tap/contents/README.md -f sha=<current> -f content=<base64>. -->

# MLReps Homebrew tap

The Homebrew tap for the **MLReps** command-line tool — a codebase auditor and merge guard.

→ **https://www.mlreps.com**

```sh
brew install mlreps/tap/mlreps
```

**Available after the first release.** Until then this tap holds no formula, and the command above will
fail with *"No available formula"* — that is this page being honest rather than the tap being broken.

What works today, with Node.js 20 or newer:

```sh
npm install -g mlreps
```

## What the formula will install

A standalone build that needs no Node.js: macOS and Linux, x64 and arm64. It is pinned to the exact
archives of one release in **[mlreps/cli](https://github.com/mlreps/cli)**, by SHA-256, and generated
from that release's own `SHA256SUMS` — so the formula cannot name a checksum no release published.

The macOS builds are **ad-hoc signed and not notarized**, which Homebrew does not require and which
installing through `brew` does not trip over.
[mlreps/cli](https://github.com/mlreps/cli#verifying-a-download) says what the checksum proves, what it
does not, and why there is no public build attestation to check yet.

The formula carries `license :cannot_represent`: the CLI is not open source, and the licence it ships
under has no SPDX identifier Homebrew can express. That is also why this is a tap of our own and not a
submission to homebrew-core, which takes only software whose source is public and buildable from source.

## Issues are off here

A tap is a file of checksums; a problem with it is almost always a problem with the release it points at.
Write to **connect@mlreps.com**.
