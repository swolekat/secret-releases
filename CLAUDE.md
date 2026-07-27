# Secret Releases

Static one-page site ([index.html](index.html)) listing unsigned personal builds.
Published with GitHub Pages from `main`.

## Rules

### All downloads must be hosted in this repo's releases

Every download link on the page **must** point at
`https://github.com/swolekat/secret-releases/releases/download/...`.

Never link to another repository's releases (e.g.
`github.com/swolekat/VrmBoneTool/releases/...`), and never link to any other
external host. If a tool lives in its own repo, download the artifact from that
repo's release and re-upload it as an asset here, then point the page at the
copy in this repo.

Why: this page is the single distribution point. Links to other repos break when
those repos are renamed, made private, or have their releases retidied, and they
expose repo names that aren't meant to be advertised from here.

### This repo has to stay public

Release assets inherit the repo's visibility. While this repo was private every
download link on the page 404'd for visitors, even though the Pages site itself
served fine. "Secret" here means *unlisted* — `noindex, nofollow` on the page,
not linked from anywhere — not private. Don't flip it back.

The tool repos (`VrmBoneTool`, `VnyanHandColliders`, …) stay private; that's the
other reason artifacts get re-uploaded here rather than linked.

### Releases are just asset buckets — bump the patch version

Release tags here (`v0.0.1`, `v0.0.2`, …) carry no meaning beyond "a place to
attach files". To publish new artifacts, cut the next patch tag
(`gh release create v0.0.N --title "..." --notes "..." <files>`) and attach them.
Existing releases stay untouched so old links keep working.

The version badge on each card is the *tool's* version, unrelated to the release
tag it happens to be attached to.
