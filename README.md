# weightscheck-site

The landing, privacy and support pages for **Weights Check**, the diver weighting library
for iPhone. Plain static HTML, served by GitHub Pages from `main` / root — the same
arrangement as `turnpressure-site` and `timetosurface-site` in the planners' repository. No
build step.

- <https://ligrimp-lang.github.io/weightscheck-site/>
- <https://ligrimp-lang.github.io/weightscheck-site/privacy.html>
- <https://ligrimp-lang.github.io/weightscheck-site/support.html>

Apple requires the first two to be reachable at public URLs — a privacy policy under
Guideline 5.1.1(i) even though this app collects nothing, and a support URL on the listing. A
reviewer opens both, and **they must not 404**: a dead privacy-policy URL is a rejection.

Every link between the pages is relative, so the site works from that subpath, from a custom
domain, and from `open index.html` on this machine without a server.

## This folder is the source — the GitHub repo is a publishing target

The pages live in the `weights_check` repository, at `weightscheck-site/`, because no project
file lives outside the project folder (Rustam, 2026-08-26). Edit them here.
`ligrimp-lang/weightscheck-site` is only where they get published to, and a clone of it is not
a place to make changes — that is the drift this arrangement removes.

The identifiers are already in `.claude/skills/ship/scripts/app-config.sh` as
`APP_SITE_DIR`, `APP_SITE_REPO` and `APP_SITE_URL`. `publish-site.sh` was carried over from
the planners on 2026-09-03, with the version 1.0 submission, and takes the app slug like
every other ship script:

    .claude/skills/ship/scripts/publish-site.sh weights-check --dry-run   # what would change
    .claude/skills/ship/scripts/publish-site.sh weights-check             # commit and push

It refuses to publish uncommitted changes, so what is on the web always names a commit in the
project repository.

## What the wording is bound by

This is a diving app, and the pages inherit the app's own doctrine rather than restating it
loosely. No page calls a rig safe, correct or acceptable, or offers any wording that reads as
a verdict on a diver's weighting; the app's silence below the warning threshold is a safety
property and the site must not complete the symmetry either. Estimates are named as
estimates, a refusal is described as a refusal, and nothing here claims the app substitutes
for a check in the water, a dive computer or training. The full rules are in the project's
`CLAUDE.md`.

The privacy policy text has no second copy anywhere — `privacy.html` is it. The support
address, `weightscheck@ismailov.net`, matches `SupportContact.address` in `App/`.

---

© 2026 Rustam Ismailov. All rights reserved. The text and design here are published so Apple
and users can read them, not as an open-source release.
