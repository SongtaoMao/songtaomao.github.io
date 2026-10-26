# Website maintenance instructions

## Scope and source of truth

- This directory is the standalone repository `SongtaoMao/songtaomao.github.io`.
- Before any Git mutation, verify that `git rev-parse --show-toplevel` is this website directory and `origin` is the website repository. Use an explicit working directory or `git -C`; the surrounding workspace belongs to an unrelated repository.
- Read `README.md` and the latest entry of `RESULT.md` before continuing work.
- The live site is https://songtaomao.github.io/ and publishes from `main /`.
- Preserve the current hosting provider and repository identity unless the user requests a change.

## Editing and publication

- The established workflow for visible website changes is preview first, publish after user confirmation. Work on `codex/<task>` branches and push the work there while awaiting publication.
- A current explicit publish request authorizes publication without asking again.
- While the site is intended to remain online, maintenance documentation alone may be committed and pushed to main; verify that no unreviewed website changes are included. During an active pause, push documentation to a non-production branch as well, to avoid accidentally redeploying the site.
- Do not infer a shutdown request from historical references to pausing the website.
- For an explicitly requested pause, preserve the latest version and settings, then ensure the public site is unavailable / 404. Do not replace it with a maintenance message.
- Never restore the August 2026 backup by default; use the latest intended snapshot.
- Preserve existing layout choices, author ordering, publication links, SEO metadata, and Search Console verification unless the requested edit requires changes.

## Work and synchronization

- Keep local work limited to lightweight edits, status checks, small inspections, and short previews.
- Push scripts/configuration to GitHub before expensive execution. Run heavy jobs in GitHub Codespaces or another GitHub-side runner when available.
- Avoid long local Python runs unless the user explicitly permits them.
- After each round, update `RESULT.md`, commit the scoped changes, and push the appropriate branch. Record what was checked, what was published, and any unresolved limitations.
- Check remote updates before pushing; avoid force pushes and unrelated files.
- Treat this as a public repository: keep private chat links, machine-local paths, credentials, and unpublished application material out of tracked files.
- There is no configured Overleaf remote for this website. Synchronize source documents separately only when they are part of the task, and report actual synchronization accurately.
