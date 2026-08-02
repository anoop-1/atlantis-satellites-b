# Atlantis NDT backlink satellites (overflow set)

Eleven of the 35 atlantisndt.com satellites live here rather than in
`anoop-1/atlantis-reimagined1/backlink-sites/`.

**Why a second repo.** Vercel caps the number of projects that may be
git-linked to a single repository. The main repo reached that cap at 24
projects (the main site plus 23 satellites), so these eleven could not be
connected there and would have had no auto-deploy.

**Source of truth is still the main repo.** `backlink-sites/<name>` in
`atlantis-reimagined1` remains where these sites are edited; a workflow in that
repo mirrors changes here on push, which is what triggers the Vercel build.
Do not edit these folders directly — the next mirror run will overwrite them.

Each directory is an independent Next.js app and its own Vercel project, served
at `https://<name>.vercel.app`.
