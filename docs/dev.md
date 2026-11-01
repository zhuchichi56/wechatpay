# Development Log

## 2026-11-01 — Install the WeChat bill analyzer on the local Mac

- **Question:** Install the upstream WeChat bill analyzer as a local Mac application and prepare to analyze the user's WeChat spending.
- **Analysis / Root Cause:** The upstream repository has no published GitHub release. The local Mac uses Apple Silicon, so a native arm64 application must be built from source. The user has not exported a personal bill yet.
- **Solution:** Installed the native arm64 application at `/Users/zhuhe/Applications/微信账单分析工具.app`. Built with `CSC_IDENTITY_AUTO_DISCOVERY=false npx electron-builder --mac --dir --arm64 -c.mac.icon=null`, using the default icon because upstream icon files are absent, then applied a local ad-hoc signature. Explained how to export a personal reconciliation bill from WeChat. Personal bills remain outside this repository.
- **Files Changed:** `docs/dev.md`; build outputs and dependencies are ignored by Git.
- **Validation:** All 31 existing tests, TypeScript checks, and Vite renderer build passed. macOS deep/strict signature verification passed. Main and renderer processes run, and CUA screenshot verification shows the welcome page, bill import button, and analysis navigation. No personal bill has been imported.
- **Commit Hash:** Initial installation record: `0cd51e5`. Final validation is recorded in the commit containing this update.
