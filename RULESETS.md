# GitHub Rulesets Configuration

Rulesets must be configured via GitHub UI (Settings → Rules → Rulesets). This file documents the intended configuration.

---

## Ruleset: `main-protection`

**Target:** `main` branch
**Applies to:** All repos in the totakit org

### Rules

| Rule | Setting |
|------|---------|
| Restrict deletions | ✅ Enabled |
| Restrict force pushes | ✅ Enabled |
| Require pull request | ✅ Enabled |
| Required approvals | 1 |
| Dismiss stale reviews | ✅ Enabled |
| Require CODEOWNERS review | ✅ Enabled |
| Require conversation resolution | ✅ Enabled |
| Require status checks | ✅ build, lint, typecheck |
| Require linear history | ❌ Disabled |
| Require signed commits | ❌ Disabled |

### Bypass List

| Actor | Bypass Mode |
|-------|-------------|
| Repository Admin | Always |

### How to Import

1. Go to Settings → Rules → Rulesets
2. Click New ruleset → Import a ruleset
3. Upload `rulesets/main-protection.json`
4. Review and save

### Why These Settings

- Require PR: All changes are reviewed and documented
- CODEOWNERS review: Maintainer sees all changes
- Status checks: No broken code reaches main
- Admin bypass: Quick fixes without ceremony when needed
- No signed commits: Reduces friction for contributors
- No linear history: Allows merge commits (easier for beginners)

### Future Additions

When CI matures:
- Require `lighthouse` status check (performance budget)
- Require `security` status check (dependency audit)
- Require `a11y` status check (accessibility)
