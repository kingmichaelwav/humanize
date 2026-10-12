# My humanize skills (fork of harshaneel/humanize)

This is my personal copy. I own it and can edit it freely.

## What's in here

    humanizer/                          <- MY main skill (the one Claude uses as "humanizer")
                                           blader/humanizer 3.1.0 + harshaneel's rules, merged 2026-10-12
    plugins/humanize/skills/ai-check/   <- the "does this sound AI?" scorer (used as "ai-check")
    plugins/humanize/skills/humanize/   <- harshaneel's original humanize skill, untouched (reference)

On my Windows PC, `~/.claude/skills/humanizer` and `~/.claude/skills/ai-check` are
junctions (folder links) pointing into this repo at `C:\Users\KING\humanize`, so edits
here are live on the next skill run. Old pre-merge copy: `~/.claude/skill-backups/`.

## Save my own edits to GitHub

    cd ~/humanize
    git add -A && git commit -m "my tweak" && git push

## Pull harshaneel's latest (only when I want it)

    git fetch upstream
    git log main..upstream/main --oneline     # see what's new first
    git merge upstream/main
    git push

His changes land in `plugins/` and won't touch `humanizer/`. If he improves his
humanize rules, port the good parts into `humanizer/SKILL.md` by hand.

## Pull blader's latest (the base of humanizer/)

blader/humanizer is not a git remote here. Download its SKILL.md, compare it with
`humanizer/SKILL.md`, and keep my additions: the "Final gate" section, section G
(§27 to §32), "Fitting the register", and "Writing new text". Notes on what came
from where are in `humanizer/README.md`.
