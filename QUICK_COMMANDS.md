# ⚡ Quick GitHub Commands Reference

Essential commands for daily GitHub workflow.

---

## 🔄 Daily Workflow

### Quick Commit
```bash
git add .
git commit -m "💚 Daily update - $(date +'%Y-%m-%d')"
git push
```

### Update with Timestamp
```bash
echo "✅ $(date)" >> daily-log.txt
git add . && git commit -m "📝 Daily log update" && git push
```

---

## 🌿 Branch Management

### Create & Switch to New Branch
```bash
git checkout -b feature/new-feature
```

### Push New Branch
```bash
git push -u origin feature/new-feature
```

### List All Branches
```bash
git branch -a
```

### Delete Local Branch
```bash
git branch -d branch-name
```

---

## 📝 Commit Message Emojis

| Emoji | Code | Usage |
|-------|------|-------|
| ✨ | `:sparkles:` | New feature |
| 🐛 | `:bug:` | Bug fix |
| 📝 | `:memo:` | Documentation |
| 🚀 | `:rocket:` | Deployment |
| ♻️ | `:recycle:` | Refactoring |
| 🎨 | `:art:` | UI/Style |
| ⚡ | `:zap:` | Performance |
| 🔧 | `:wrench:` | Configuration |
| 💚 | `:green_heart:` | CI/Build |
| 🤖 | `:robot:` | Automation |

---

## 🔍 Useful Git Commands

### Check Status
```bash
git status
```

### View Commit History
```bash
git log --oneline --graph --all
```

### Undo Last Commit (Keep Changes)
```bash
git reset --soft HEAD~1
```

### View Remote URL
```bash
git remote -v
```

### Pull Latest Changes
```bash
git pull origin main
```

---

## 🚀 GitHub CLI Commands

### Create New Repo
```bash
gh repo create repo-name --public
```

### View Issues
```bash
gh issue list
```

### Create Issue
```bash
gh issue create --title "Issue title" --body "Description"
```

### View PRs
```bash
gh pr list
```

### Create PR
```bash
gh pr create --title "PR title" --body "Description"
```

---

## 📊 Repository Stats

### Count Commits
```bash
git rev-list --count HEAD
```

### Contributors
```bash
git shortlog -sn
```

### File Changes
```bash
git diff --stat
```

---

## 🔧 Configuration

### Set Username
```bash
git config --global user.name "Your Name"
```

### Set Email
```bash
git config --global user.email "your@email.com"
```

### View Config
```bash
git config --list
```

---

## 💡 Pro Tips

### 1. Alias for Quick Commits
Add to `.bashrc` or `.zshrc`:
```bash
alias gac='git add . && git commit -m'
alias gp='git push'
```

Usage:
```bash
gac "Update README" && gp
```

### 2. Auto-push Script
Create `quick-push.sh`:
```bash
#!/bin/bash
git add .
git commit -m "${1:-Quick update}"
git push
```

Usage:
```bash
./quick-push.sh "My commit message"
```

### 3. Daily Log Script
Create `daily-log.sh`:
```bash
#!/bin/bash
echo "✅ Daily update - $(date)" >> daily-log.txt
git add daily-log.txt
git commit -m "💚 Daily log - $(date +'%Y-%m-%d')"
git push
```

---

## 🎯 Quick Actions

### Today's Quick Win
```bash
# Update README
echo "\n## Latest Update: $(date +'%Y-%m-%d')" >> README.md
git add README.md
git commit -m "📝 Update README with latest date"
git push
```

### Weekly Summary
```bash
# Create weekly summary
echo "# Week $(date +'%U') Summary\n\n$(date)" > weekly-summary.md
git add weekly-summary.md
git commit -m "📊 Add week $(date +'%U') summary"
git push
```

---

**Last Updated**: October 31, 2025

*Keep these commands handy for quick daily contributions! ⚡*
