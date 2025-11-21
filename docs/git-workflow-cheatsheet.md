# Git Workflow Cheat Sheet – Delta Moves Capital
**Location:** `docs/git-workflow-cheatsheet.md`

A concise, safe, and standardized Git workflow for your local Windows environment.

---

## 1. Set Repo Folder
Always start from the repo root:
```powershell
Set-Location "C:\Users\Trader\OneDrive\MergedLibrary\Merged\LocalRepos\DeltaMoves-TradingMasterNotebook"
```

---

## 2. Check Repo Status
```powershell
git status
```

---

## 3. Add / Stage Changes
Add all changes:
```powershell
git add .
```

Add a single file:
```powershell
git add path\to\file.md
```

---

## 4. Commit
```powershell
git commit -m "Describe your change here"
```

Amend last commit (if not pushed):
```powershell
git commit --amend
```

---

## 5. Push to GitHub
```powershell
git push
```

Set upstream (first push per branch):
```powershell
git push -u origin main
```

---

## 6. Pull Latest Changes
```powershell
git pull
```

Rebase pull (cleaner history):
```powershell
git pull --rebase
```

---

## 7. Creating a Branch
```powershell
git checkout -b feature-name
```

---

## 8. Switching Branches
```powershell
git checkout main
git checkout feature-name
```

---

## 9. Merging a Branch
```powershell
git checkout main
git pull
git merge feature-name
git push
```

---

## 10. Deleting a Branch
Local:
```powershell
git branch -d feature-name
```
Remote:
```powershell
git push origin --delete feature-name
```

---

## 11. View History
```powershell
git log --oneline --graph --decorate
```

---

## 12. Fixing Common Issues
Undo last commit (keep changes staged):
```powershell
git reset --soft HEAD~1
```

Undo last commit (discard changes):
```powershell
git reset --hard HEAD~1
```

Unstage a file:
```powershell
git restore --staged filename
```

Restore a deleted file:
```powershell
git checkout HEAD -- filename
```

---

## 13. GitHub CLI (gh) Examples
Create repo:
```powershell
gh repo create DeltaMoves-TradingMasterNotebook --public --source . --remote origin --push
```

List repos:
```powershell
gh repo list Delta-Moves-Capital
```

---

## 14. Pre-Commit Checklist
Before committing:
- Run `git status`
- Verify correct branch
- Ensure only intended files are staged
- Run formatters/linters
- Ensure commit message is clean and descriptive

---

## 15. Commit Message Standards
Use imperative tone:
- `Add SPX IC rotation manual`
- `Update wing width calculator`
- `Fix path issue in README`

---
