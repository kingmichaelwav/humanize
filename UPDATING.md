# My humanize skill (forked from harshaneel/humanize)

This is my personal copy. I own it and can edit it freely.

## Update MY knowledge (my own edits) — takes effect instantly
Edit any file, e.g.:
  humanize/SKILL.md              <- the humanize rules
  humanize/references/research.md<- the research notes
  ai-check/SKILL.md              <- the detector/scoring rules
The skills are symlinked into ~/.claude/skills, so edits are live on the next skill run.
(Optional) save a snapshot:  git add -A && git commit -m "my tweak"

## Pull harshaneel's latest knowledge — only when I want it
  cd ~/humanize
  git fetch upstream
  git merge upstream/main      # or: git pull upstream main
Review first if you like:  git log upstream/main --oneline -20

## Make it a GitHub fork later (optional)
Fork on github.com, then:
  git remote add origin https://github.com/<you>/humanize.git
  git push -u origin main
