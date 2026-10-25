# Daily Crypto Report (now weekly)

Version history of the DailyCryptoReport skill and its scheduled task.

| File here | Lives on disk at |
|---|---|
| `SKILL.md` | `~/.claude/skills/DailyCryptoReport/SKILL.md` |
| `scheduled-task/SKILL.md` | `~/.claude/scheduled-tasks/daily-crypto-report/SKILL.md` (runs weekly, Saturday 11:00 Europe/Paris) |

Since 2026-10-31 the report is **weekly**: it covers the previous 7 days, has a Top 10 instead of a Top 5, and allows up to 10 items per section (was about 3). The skill and task keep their `Daily…` names so existing paths and invocations keep working. The schedule itself is set in Claude Code's scheduled-task settings, not in these files: cron `0 11 * * 6`, with the Mac's time zone set to Europe/Paris.

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
