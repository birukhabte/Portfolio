---
description: Auto-commits all changes in the Portfolio directory
---
// turbo-all

1. Add all changes to git
git add .

2. Commit changes with a timestamp
git commit -m "Auto-commit: $(Get-Date -Format 'yyyy-MM-dd HH:mm:ss')"
