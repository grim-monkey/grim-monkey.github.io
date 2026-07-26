# Repository instructions

This repository publishes a static GitHub Pages site.

## Git and publishing safety

- Never add `Co-authored-by` trailers or otherwise identify an AI agent as a co-author in commit messages.
- Always create or switch to a dedicated task branch before making changes. Do not work directly on `main`.
- Commit early and often using small, focused commits that each leave the repository in a coherent state.
- Obtain the user's explicit confirmation immediately before every `git push` or other operation that updates a remote. Earlier approval, a general instruction to publish, or approval from another task does not count.
- Before requesting confirmation for any remote push:
  1. Review `git status`, including untracked and ignored files.
  2. Re-scan filenames and staged content for credentials, API keys, tokens, private keys, environment files, and other secrets.
  3. Verify `.gitignore` covers all local, generated, or sensitive files discovered by that review; update it before pushing when needed.
  4. Inspect the exact commits and diff that will be pushed.
- Never push if a suspected secret or credential is present. Stop and ask the user how to proceed.

## Branch integration

- Keep task branches short-lived and narrowly scoped.
- Regularly compare the task branch with `main` and incorporate current `main` before the branches diverge significantly.
- Suggest pushing the task branch for review and merge at these optimal checkpoints:
  1. After the first complete, tested unit of work.
  2. Before beginning a separate feature or broad refactor.
  3. Whenever `main` has advanced enough to create meaningful divergence.
  4. At the end of each working session.
  5. As soon as the branch is tested, reviewable, and ready to merge.
- Prefer multiple small branches and merges over a long-running branch.
- A suggestion to push is not permission to push. Obtain explicit confirmation immediately before every push.

## Site structure

- Check all HTML and CSS asset references before moving or renaming files.
- Preserve published URLs when reorganizing assets, or update and validate every affected reference in the same change.
