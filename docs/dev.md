# Development Log

## 2026-11-01 — Install the WeChat bill analyzer on the local Mac

- **Question:** Install the upstream WeChat bill analyzer as a local Mac application and prepare to analyze the user's WeChat spending.
- **Analysis / Root Cause:** The upstream repository has no published GitHub release. The local Mac uses Apple Silicon, so a native arm64 application must be built from source. The user has not exported a personal bill yet.
- **Solution:** Build the renderer and Electron application locally, install the resulting application in the user's Applications folder, and verify launch. Explain how to export a personal reconciliation bill from WeChat. Personal bills remain outside this repository.
- **Files Changed:** `docs/dev.md`; build outputs and dependencies are ignored by Git.
- **Validation:** Installation and launch verification in progress.
- **Commit Hash:** Pending; the installation record will be committed after validation.
