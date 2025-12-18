# 🚀 Showcase Sync Instructions

**This file lives in the submodule itself so Copi sees it when working here.**

---

## Quick Push (From Showcase Folder)

```bash
cd NovaLiveSystem-Showcase
git add -A
git commit -m "your message"
git push origin main
```

Then update the parent repo's reference:
```bash
cd ..
git add NovaLiveSystem-Showcase
git commit -m "chore: Update showcase submodule"
git push origin main
```

---

## VS Code Task (Easiest)

`Ctrl+Shift+P` → "Tasks: Run Task" → **"Sync: Showcase to Public Repo (PUSH)"**

---

## Important Notes

1. **This is a SUBMODULE** - it has its own `.git` and pushes to `NovaLiveSystem-Showcase-PUBLIC`
2. **The main repo tracks a commit pointer** - after pushing here, update the parent
3. **Clean history** - this repo was reset on 2025-12-18 to remove exposed secrets
4. **Remote:** `https://github.com/SparkSupernova/NovaLiveSystem-Showcase-PUBLIC.git`

---

## What Goes Here (Curated Content Only)

✅ README, architecture docs, screenshots
✅ Public-facing documentation
✅ Training results summaries
✅ Roadmap, changelog, FAQ

❌ NO source code from nova/
❌ NO API keys or secrets
❌ NO private artifacts or datasets
