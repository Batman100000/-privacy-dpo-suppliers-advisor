# 🔐 Security Guidelines

## ⚠️ CRITICAL: Never Commit Secrets!

### What to Never Commit:
- ❌ GitHub tokens (ghp_*)
- ❌ API keys
- ❌ Passwords
- ❌ Private credentials
- ❌ .env files
- ❌ .git-credentials

### Safe Ways to Use Tokens:

#### Option 1: Environment Variable (Recommended)
```bash
export GITHUB_TOKEN="your_token_here"
git push https://oauth2:${GITHUB_TOKEN}@github.com/...
```

#### Option 2: .env File (Local Only)
```bash
cp .env.example .env
# Edit .env with your token
source .env
git push https://oauth2:${GITHUB_TOKEN}@github.com/...
```

#### Option 3: SSH Keys (Most Secure)
```bash
# Generate SSH key
ssh-keygen -t ed25519 -C "your_email@example.com"
# Add to GitHub: https://github.com/settings/keys
git push git@github.com:Batman100000/-privacy-dpo-suppliers-advisor.git main
```

---

## Incident History

### ❌ Token Exposure (2026-08-08)
- **Issue:** Token stored in ~/.git-credentials
- **Token:** ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxx
- **Action:** REVOKED immediately
- **Fix:** 
  - Removed .git-credentials
  - Disabled credential.helper=store
  - Added .gitignore

### ✅ Remediation Applied
- All secrets removed from:
  - Repository files
  - Git history
  - Local filesystem
- New .gitignore added
- .env.example template created

---

## Recommendations

1. **Always use SSH keys** for git operations (most secure)
2. **Never use git credential.helper=store** (plain-text storage)
3. **Always add sensitive files to .gitignore**
4. **Review commits before pushing** (check for secrets)
5. **Rotate tokens regularly** (every 90 days)
6. **Use environment variables** for temporary tokens

---

## Testing for Secrets

```bash
# Search repo for common secret patterns
git log -p | grep -i "ghp_\|password\|apikey\|secret"

# Check for exposed files
grep -r "ghp_" .git*
grep -r "password" *.html *.js
```

---

## For Developers

Before committing:
```bash
# Pre-commit hook to prevent accidental secret commits
git diff --cached | grep -E "ghp_|password|apikey|secret" && echo "❌ Secrets found!" || echo "✅ Safe to commit"
```

