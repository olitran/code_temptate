# Source-only GitHub backup policy

- GitHub is a source backup for this project. Track authored code, source notebooks,
  tests, documentation, dependency manifests/lockfiles, and portable configuration
  templates needed to rebuild and maintain it. Keep only required source assets and
  small, synthetic test fixtures; do not use these exceptions for runtime data.
- Keep datasets, databases, user/private data, credentials, local configuration,
  model weights, downloaded dependencies, virtual environments, caches, logs,
  generated reports/evidence, screenshots, notebook outputs, compiled bundles,
  installers, archives, and backup directories out of Git. Keep necessary local
  files on disk and ignored. Clear notebook execution outputs before committing.
- Maintain targeted `.gitignore` rules. Inspect `git status` and the staged diff
  before every commit; stage explicit paths and never force-add excluded content.
  Ignore rules do not untrack existing files. Remove existing non-source files from
  the index only in a reviewed cleanup that preserves local copies and working
  application requirements. Never rewrite shared history or force-push to reclaim
  storage without the owner's explicit approval.
- Keep GitHub Actions disabled for this repository. Do not enable, dispatch, or add
  automatic CI, scheduled jobs, build/release/deployment workflows, artifact
  uploads, or Actions caches unless the owner explicitly requests an exception.
  Ordinary Git pushes are the backup mechanism and need no Actions runs.
- Run required lint, tests, builds, and synthetic checks locally. Keep their output
  local; report results concisely in the conversation. Do not upload generated
  output through Git LFS, GitHub Releases, Packages, or other GitHub storage as a
  workaround. An exception must specify the intended compute/storage use.
- This owner policy overrides older instructions to run hosted CI, publish build
  evidence, or wait for Actions after a push. Preserve applicable local validation
  requirements. It grants no permission to delete local user data, publish unrelated
  changes, or create releases.
