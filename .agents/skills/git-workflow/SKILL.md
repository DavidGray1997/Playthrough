---
name: git-workflow
description: Safely review, commit, publish, or merge repository changes, with strict privacy checks for public repositories.
---

# Git workflow

Use this skill before committing, pushing, opening or updating a pull request, merging, or otherwise publishing repository changes. Treat every pushed branch and pull request as public and potentially persistent, even when the repository or PR is later closed.

## Establish scope

1. Inspect the repository root, current branch, remotes, mainline, status, and documented contribution process.
2. Separate pre-existing work from changes made for the current task. Do not discard, stage, or publish unrelated user changes.
3. Prefer a feature branch and pull request for delivery to `main`. An explicit request to deliver code does not imply product acceptance or release authorization.

## Public-content privacy gate

Before staging or publishing, review the complete intended diff, including modified and new files, documentation, tests, assets and metadata. Check both the worktree and the exact staged blobs; compare the staged file list with the reviewed file list.

Do not publish:

- Credentials, tokens, private keys, authentication/configuration dumps, private hostnames, personal home-directory paths, live user/catalogue data, or sensitive logs.
- Personal identifying information that is not required and explicitly approved for publication.
- Raw user prompts, conversation excerpts, assistant/tool context, or copied instructions. This includes short approval quotes used as decision evidence. Record the responsible role, decision status, date, rationale, and a durable decision/evidence reference instead; paraphrase without reproducing the conversation.
- Temporary handover/continuation notes, scratch files, generated build output, or unrelated local artifacts.

Use available secret scanners and targeted pattern checks, then manually inspect all changed content. Check images and other binary artifacts for embedded metadata or visible personal information when they are in scope. Keep third-party package provenance and licences when required; do not mistake public package metadata for project-user data.

If any content is ambiguous, the reviewed file set does not exactly match the staged set, or the audit cannot cover the complete intended output, stop before commit/push and ask for clarification. Never describe a scan as proof of “100% certainty”; state its scope and limits.

## Delivery checks

- Stage only reviewed, intended files; do not use blanket staging when unrelated or temporary files are present.
- Recheck the staged names, full staged diff, whitespace, sensitive-content scan, and commit author/committer identities immediately before committing.
- Use the repository's established commit, review, PR, merge, and co-author conventions. Do not amend or rewrite published history unless explicitly authorized.
- Before merging, check the target branch, PR diff, required reviews/checks, and mergeability. After merge, verify the resulting mainline commit and its published author/committer metadata.
- Do not imply that merging is a release or that a task is accepted unless its separate acceptance criteria and authority are evidenced.

## If sensitive content was published

Stop further publication immediately. Close the PR and delete its source branch to limit further exposure, but do not claim that this erases the PR: GitHub may retain pull-request refs such as `refs/pull/<number>/head`, cached diffs, or commit objects. For removal of exposed content, use GitHub's sensitive-data removal process and report what remains publicly accessible or uncertain. If a credential was exposed, arrange revocation/rotation; deleting a branch is not sufficient.
