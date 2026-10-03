---
name: update-github-info

on:
  schedule: daily
  workflow_dispatch:

permissions:
  contents: read

tools:
  edit:
  web-fetch:

network:
  allowed:
    - github.blog
    - github.com

safe-outputs:
  create-pull-request:
---

# Update GitHub Info

Keep the GitHub information page current with useful updates for developers.

1. Read `notes/mona-notes.md` and follow Mona's editorial guidance.
2. Fetch https://github.blog/latest/ with the web-fetch tool.
3. Fetch https://github.blog/changelog/ with the web-fetch tool.
<<<<<<< HEAD
4. Review the fetched sources for recent, practical updates that help developers learn GitHub faster.
5. Update `site/content/github-info.md` with concise summaries and links to the original GitHub Blog or GitHub Changelog sources. Preserve the file's existing style and avoid unrelated changes.
6. If the sources do not warrant an update, make no edits and report that no pull request is needed.
7. If the file changed, use the `create-pull-request` safe output to open a pull request for Mona to review. Summarize what changed and cite the source links in the pull request body. Do not write directly to `main`.
=======
4. Web fetch https://awesome-copilot.github.com/workflows/.
5. Review the fetched GitHub Blog, GitHub Changelog, and Awesome Copilot workflow sources for recent, practical updates that help developers learn GitHub faster.
6. Update `site/content/github-info.md` with concise summaries and links to the original GitHub Blog, GitHub Changelog, or Awesome Copilot sources. Preserve the file's existing style and avoid unrelated changes.
7. If the sources do not warrant an update, make no edits and report that no pull request is needed.
8. If the file changed, use the `create-pull-request` safe output to open a pull request for Mona to review. Summarize what changed and cite the source links in the pull request body. Do not write directly to `main`.

## Updater request

Web fetch https://awesome-copilot.github.com/workflows/ and update `site/content/github-info.md` with a noteworthy Awesome Copilot workflow, citing that URL as the source.
>>>>>>> ab51909 (Fix Awesome Copilot updater request)
