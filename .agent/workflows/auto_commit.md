---
description: Auto-commits all changes in the Portfolio directory
---
// turbo-all

1. Navigate to the Portfolio directory
cd C:\Frontend_Projects\Portfolio

2. Loop through changed files, add and commit each one individually
$changedFiles = git status --porcelain | ForEach-Object { $_.Substring(3).TrimStart().Trim('"') }
foreach ($file in $changedFiles) {
    if ($file) {
        git add "$file"
        git commit -m "changes made : $file"
    }
}
