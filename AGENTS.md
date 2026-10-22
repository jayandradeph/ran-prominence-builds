# Public RAN Prominence builder

- This repository contains only README.md, AGENTS.md and .github/workflows/build.yml.
- Keep source, assets, keys, compiler output, binaries and caches private.
- Keep manual-only triggers and one resolved private source commit for all jobs.
- Keep credentials ephemeral and repository-scoped; never print secret values.
- Android jobs validate shared data portability; the iOS job builds the separate online Game IPA. Device runtime acceptance is separate.
- Commit, push, publish or create pull requests only when explicitly requested.
