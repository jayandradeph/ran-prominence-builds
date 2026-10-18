# RAN Prominence builds

Public orchestration only. Game source, assets, compiler logs, libraries, apps,
debug symbols and signing credentials do not belong in this repository.

This is a prepared builder for a port in progress. Windows builds Game.exe and
Emulator.exe. Android ARM64/x86-64 and iOS ARM64 currently build only the shared
hash and asset-codec libraries/probes. A green mobile job does not produce a playable
game, APK or IPA. Servers and editors remain Windows-only.

An administrator must configure `PROMINENCE_SOURCE_REPOSITORY` as the private
owner/repository, and repository secret `PROMINENCE_SOURCE_TOKEN` with contents
read/write access to that private source repository. Prefer a fine-grained token
limited to that repository. The token is used to
check out reviewed main and deliver private draft releases. Never store it as a
variable or paste it into files. Keep workflow write access restricted.

Run **Build RAN Prominence (port in progress)** manually. Every selected job uses
one resolved main commit. There are no PR triggers, public artifacts or caches.
Products, result.json, hashes and compiler logs are uploaded to draft releases
in the private source repository. Failed builds deliver diagnostics without
claiming success. Cloud validation is in progress. iOS signing and device installation are separate work.

Export only this README, AGENTS.md and `.github/workflows/build.yml` into the
public repository. Do not publish the surrounding private source workspace.
