# yikang-shareable

Public mirror for docs / skills / snippets I want to pull onto machines that can't reach gist or private repos (e.g. work laptop on a restricted network).

## How to add a new entry (SOP)

1. `cd ~/projects/yikang-shareable && git pull --ff-only`.
2. Pick a folder name `YYYYMMDD###-<slug>`:
   - `YYYYMMDD` — today's date.
   - `###` — 3-digit daily counter, starts at `001`, increments for each new folder added today.
   - `<slug>` — kebab-case description of what it is (not where it came from). E.g. `llm-wiki`, `codex-cli-setup`.
3. Create the folder. Put the main content in `README.md` inside it. Support files (images, extra `.md`, scripts) alongside.
4. **Sensitive info scan** on everything about to be committed:
   - Secrets: `sk-`, `ghp_`, `gho_`, `AKIA`, `xox[bp]-`, `Bearer `, `api[_-]?key`, `password\s*=`
   - Emails other than my own
   - Internal IPs: `192.168.`, `10.\d+\.`, `100.\d+\.` (Tailscale), `127.0.0.1`
   - Private absolute paths (rewrite `/Users/yluo/...` → `~/...`)
   - Company / internal proper nouns — repo name and content stay neutral (no `jpm`, client names, internal codenames).
5. Update this README:
   - **Index**: add the new folder under its topic category (alphabetical within category; add a new `### Category` if none fits).
   - **Log**: prepend `## [YYYY-MM-DD] <folder> — <one-line>` at the top of the log section.
6. `git add -A && git commit -m "add <folder> — <one-line>" && git push origin main`.

Folder names are permanent — never rename. If something's wrong, add a correction folder and cross-link.

## Index

Content catalog, grouped by topic.

### AI / LLM workflow
- [`20260421001-llm-wiki/`](20260421001-llm-wiki/) — pattern for an LLM-maintained, persistent personal knowledge base (mirrored from a Karpathy-style gist).

## Log

Append-only, newest first. Format: `## [YYYY-MM-DD] <folder> — <one-line>`

## [2026-04-21] 20260421001-llm-wiki — mirror of public gist 4d78480 (llm-wiki idea doc)
