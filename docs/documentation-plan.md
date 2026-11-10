# Stovepipe Website Documentation Plan

_As of 2026-11-09_

## Purpose and audience

The stovepipe-website repo needs a small set of docs so anyone can run, edit and deploy the site without having to ask. Keep them short. The site is two files today, and the docs should stay in proportion.

| Reader | What they need from the docs |
| --- | --- |
| Maintainer | How to preview, change copy and deploy in under 5 minutes |
| Future contributor or contractor | Where things live, conventions, how to submit a change |
| Whoever handles hosting | Where the site is deployed, domain and DNS settings |

## Current state

The site is a single placeholder page with no docs, no commits and no hosting yet.

- `index.html`: header, "Coming soon" hero, contact card, footer
- `styles.css`: one stylesheet with color tokens on `:root`, automatic dark mode, mobile layout
- No build step, dependencies or tests
- Gaps: no README, no deploy instructions, placeholder copy, and a placeholder contact address (`hello@stovepipeinteractive.com`)

## Planned documents

Five documents cover the site. Only the README is needed right away.

| Document | Covers | Length |
| --- | --- | --- |
| `README.md` | What the site is, file layout, how to preview locally, links to the other docs | ~1 page |
| `docs/deployment.md` | Hosting provider, how a change goes live, domain and DNS, rollback | ~1 page |
| `docs/content-guide.md` | Voice, approved copy, logo and color tokens (`--accent` etc.), contact address | ~1 page |
| `docs/contributing.md` | Branching, commit messages, review before merge, browser checks | Half a page |
| `CHANGELOG.md` | Dated list of visible site changes, newest first | Grows over time |

## Structure and location

All docs live in the repo as Markdown, so a doc change goes in the same commit as the site change it describes. The README sits at the root and links to everything in `docs/`.

```
stovepipe-website/
├── README.md          # entry point, links to docs/
├── CHANGELOG.md
├── index.html
├── styles.css
└── docs/
    ├── documentation-plan.md   # this file
    ├── deployment.md
    ├── content-guide.md
    └── contributing.md
```

Keep `docs/` out of the published site. The host should serve only `index.html`, `styles.css` and assets.

## Priorities and sequencing

Write each doc when the site reaches the milestone that needs it, not before.

1. **Now (placeholder page):** README, added with the first commit
2. **Hosting chosen:** deployment guide, written while doing the first deploy
3. **Real copy and branding:** content and brand guide; start the changelog
4. **Someone else starts contributing:** contributing guide

## Maintenance

- The maintainer owns all docs until a second contributor joins.
- Any change that alters setup, deployment or copy rules updates the matching doc in the same commit.
- Every visible change to the site gets a changelog line.
- Review all docs once a quarter, or at each milestone above, and delete anything stale.

## Open questions

- [ ] Which hosting provider: GitHub Pages, Netlify, or something else?
- [ ] What public contact address replaces `hello@stovepipeinteractive.com`?
- [ ] What does Stovepipe Interactive do, and what should the final headline and copy say?
- [ ] Is an email signup wanted later, and with which service?
