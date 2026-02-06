---
description: Auto-commits all changes in the Portfolio directory
---
// turbo-all

1. Add all changes to git
git add .

2. Commit changes with a dynamic message listing changed files
$files = git diff --name-only --cached
$fileList = $files -join ", "
git commit -m "changes made : $fileList"
