# Daily Crypto Report

Version history of the DailyCryptoReport skill and its scheduled task.

| File here | Lives on disk at |
|---|---|
| `SKILL.md` | `~/.claude/skills/DailyCryptoReport/SKILL.md` |
| `scheduled-task/SKILL.md` | `~/.claude/scheduled-tasks/daily-crypto-report/SKILL.md` (runs daily ~10am) |

The history of `SKILL.md` was split out of `pai-private` (`~/.claude`) with `git subtree split`, so only this skill's commits are here. No secrets: the skill reads `XAI_API_KEY` from `~/.claude/.env` at runtime.

## Where the reports are

- Markdown: `personal-knowledge-vault/raw/reports/crypto/YYYY-MM-DD.md` (repo `bearlusconi-bera/personal-knowledge-vault`)
- Site: https://bearlusconi-bera.github.io/crypto-reports/ (repo `bearlusconi-bera/crypto-reports`)

## Refresh after editing the skill

```bash
cp ~/.claude/skills/DailyCryptoReport/SKILL.md SKILL.md
cp ~/.claude/scheduled-tasks/daily-crypto-report/SKILL.md scheduled-task/SKILL.md
git commit -am "Sync skill" && git push
```
