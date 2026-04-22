---
name: migrate-content-ia
description: >
  Handle Hugo docs information-architecture moves: discover old vs new URLs,
  add front matter aliases (Phase 1), update in-repo links (Phase 2), validate
  and fix anchor fragments (Phase 3). Supports PR-scoped evaluation and edits,
  or a full-site follow-up. Triggers on: "IA migration", "redirects for moved
  pages", "fix links after content move", "PR-scoped link/anchor pass",
  "aliases for old URLs".
---

# Migrate content IA (redirects + links + anchors)

Use this skill when pages **move or rename** under `content/` and you must
preserve old public URLs and/or fix cross-references. Work in **phases**;
choose **PR-scoped** vs **full-site** mode per run.

**Read first:** **CLAUDE.md** / **AGENTS.md** (URL rules, vendored areas, external
links, special cases) and **hugo.yaml** (`permalinks`, `refLinksErrorLevel`,
`disablePathToLower`). For **prose and link text**, follow **STYLE.md**; for
**components, front matter, and link examples**, follow **COMPONENTS.md**.

**Related skills:** **research** helps map moves and find inbound links; **write**
commits minimal edits. Run this skill’s phases after the move is identified (or
in parallel with research for large IA work).

## Progressive disclosure (optional)

The procedure below stays in this file. If a run produces a very large
**old → new** URL table, store that table in **`reference.md`** in this skill
directory and link it from the task summary, so the agent reads the long
mapping only when needed.

## Modes

- **PR-scoped (typical for a single PR)**  
  - **Evaluation, checklists, and edits** use only `git diff` / `base...HEAD`
    files (`PR_SCOPE_FILES`).  
  - Out-of-scope findings go to a **deferred** list (issue or follow-up PR).

- **Full-site (complete migration after the PR)**  
  - Update stragglers **across the repo** (or all inbound links to moved
    sections), including config-driven `link:` fields if policy allows.  
  - Still make **minimal** edits; no drive-by rewrites.

---

## Conventions (links, anchors, redirects)

### Front matter `aliases` (redirects)

- Per **COMPONENTS.md**, `aliases` are **URLs that redirect to this page**.
- Add or **merge** on the **new canonical** page; do not drop unrelated
  entries. Match local examples: **published-style paths** (leading `/`), and
  **trailing `/`** when that matches existing pages in the same area.
- **No** speculative redirects for URLs that were never published.
- **Collision check** before adding: no other page or redirect may already
  own the same old path.
- If the site also uses **`data/redirects.yml`**, only add entries when
  project policy requires it; avoid duplicating the same old URL in
  `aliases` **and** `redirects.yml` unless maintainers do.

### Internal links in Markdown (STYLE.md + COMPONENTS.md)

- Use **relative paths to source files** (e.g. `../section/page.md`) with
  **`.md`**, following **COMPONENTS.md** examples, unless the file already
  uses an established pattern (e.g. some `link:` or nav fields use **published**
  paths without `manuals` or `.md` — **match the surrounding file**).
- Keep **CLAUDE.md** / **AGENTS.md** rules: internal ref targets under
  `content/manuals/...` often use the full **`/manuals/...`** path; published
  URLs omit the `manuals` segment—do not confuse the two when fixing links.
- **Link text (STYLE.md):** descriptive, ~**5 words**; no “click here” / “learn
  more”; **no** end punctuation **inside** the link text; **no** bold/italic
  on link text unless normal in the sentence.
- **Headings (STYLE):** **sentence case**; do not rename headings in passing
  unless the migration requires it (heading changes break fragments).

### Shortcodes and layouts (links not only in Markdown)

- **Phase 2–3 scope includes** any **shortcode or layout partial** in
  `PR_SCOPE_FILES` (or the whole repo in full-site mode) that emits links:
  e.g. `ref` / `relref`, `link` fields in shortcode args, or hardcoded
  `docs.docker.com` / path strings. Grep for old paths, slugs, and fragments
  under `layouts/shortcodes/` (and `layouts/_default/` if partials build nav).
- Match each file’s existing pattern; do not rewrite working shortcode style
  just to “clean up.”

### Fragments / anchors (Phase 3)

- Same-page: `[Text](#section-id)`.
- Cross-page: `#fragment` must match the **target** page’s **generated** heading
  ID (Hugo slugification; see CLAUDE.md / **AGENTS.md**). Validate fragments
  in shortcodes the same way as in body Markdown when the target is a migrated
  page.

### External URLs (**AGENTS.md**)

- Do not commit **guessed** replacement URLs. If a URL cannot be verified,
  treat as blocked or drop the fragment per AGENTS guidance.

### Special cases (**AGENTS.md**)

- **Engine API version** pages: respect coordinated **`/latest/` `aliases`**
  rules—never leave two version files both owning `/latest/`.
- **Vendored / generated** trees: read-only; see CLAUDE.md. Do not “fix” links
  there if policy forbids.

---

## Phase 0 — Discovery (read-only; may use whole repo)

1. Read **hugo.yaml** (permalinks, `refLinksErrorLevel`, `disablePathToLower`).
2. From the branch (diff, renames), build a **mapping table**:
   - old source path → new source path  
   - old published URL → new published URL (from permalink rules)
3. **Case:** with `disablePathToLower: true`, filesystem path **case** appears in
   URLs—**directory and link casing must match** (e.g. `setup` vs `Setup`).

---

## Phase 0.5 — PR-scoped evaluation (required before edits in PR mode)

1. **Set `PR_SCOPE_FILES` (Git scope for PR mode)**  
   - When the PR **targets `main`**, use the same triple-dot form as
     **review-changes**:  
     `git diff --name-only main...HEAD`  
   - For a **different target branch** or a custom base, use the merge base:  
     `BASE=$(git merge-base <target-branch> HEAD)`  
     then:  
     `git diff --name-only "$BASE"...HEAD`  
   - Treat the resulting paths as the only files eligible for **edits** in
     PR-scoped Phases 1–3; everything else is **deferred** unless the user
     explicitly expands scope.

2. From those files only, build checklists:
   - path/URL mapping this PR must honor  
   - links to update in this PR (Markdown **and** shortcode/layout files in scope)  
   - cross-page **fragments** pointing at targets touched by this PR
3. Items outside `PR_SCOPE_FILES` → **deferred** (no edit).

---

## Phase 1 — `aliases` (old published URLs)

1. On each **new** canonical page, add or merge **`aliases`** for every **real**
   former public URL.
2. Do not strip existing unrelated aliases.
3. **PR-scoped:** add aliases only where the canonical file is in scope or the
   project requires it; otherwise list missing alias targets for follow-up.

---

## Phase 2 — In-repo link reference updates

1. Replace old source paths or old published URLs with the **new** targets;
   preserve each file’s link pattern (relative vs root-anchored `.md` paths).
2. **Full-site:** sweep `content/` and, per **AGENTS “Page deletion
   checklist”**-style thoroughness, check **config / front matter** `link:` and
   similar so nav and grids are not left on old slugs.
3. **PR-scoped:** only update files in `PR_SCOPE_FILES`; log stragglers.
4. Include **shortcodes and layout partials** in scope (see Conventions above).

---

## Phase 3 — Anchor / fragment validation and fixes

1. For every in-scope link with `#...` to a migrated page, confirm the fragment
   against real heading IDs on the **target** page.
2. **Full-site:** fix broken fragments for all relevant inbound links.
3. **PR-scoped:** fix only in `PR_SCOPE_FILES`; defer the rest.
4. If new breaks appear, create a **new checklist** and repeat Phase 3 within
   the chosen scope.

---

## Optional: scripts helper

This skill may ship a small **scope helper** so agents do not re-derive Git
recipes. See [scripts/scope-pr-files.sh](scripts/scope-pr-files.sh) — it prints
paths in PR scope for a given target branch (default `main`).

---

## Verification

```bash
docker buildx bake validate
```
